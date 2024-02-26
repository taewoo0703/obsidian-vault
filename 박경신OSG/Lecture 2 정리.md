# ○ 스마트 포인터
- syntax와 semantics상 일반 포인터와 동일
- 메모리 관리나 locking등 좀 더 유용한 일을 수행한다.
- 예시로 cpp std의 auto ptr는 스코프를 벗어나면 객체를 delete 해주는 기능 포함
	```cpp
	void foo()
	{
		auto_ptr<MyClass> p(new MyClass);
		p->DoSomething();
	} // p가 알아서 scope를 벗어나면 clean up 해준다.
	```

## >> 스마트 포인터를 써서 얻는 점
- Automatic cleanup - 포인트를 free할 필요가 없다.
- Automatic initialize - 스마트 포인터를 `NULL`로 초기화할 필요가 없다.
- Dangling pointers
- Exception safety - try/catch를 고민하지 않아도 된다.
- Garbage collection
- Efficiency - 스마트 포인터가 가용 메모리의 사용을 좀 더 효과적으로 만들어주며 메모리 할당과 해제 시간을 줄여준다.
- STL containers

# ○ osg::ref_ptr
## >> OSG 메모리 관리
1. OSG 응용프로그램에서 scene graph 사용이 끝나면 메모리 누수(memory leak)를 피하기 위해 각 노드마다 차지하고 있던 메모리를 delete해야 한다.
2. 전체 scene graph를 traverse하면서 각 노드(와 데이터)를 delete하는 일은 매우 복잡한 일이다.
3. 이 문제의 해결 방법으로 reference counted memory를 사용한 automated garbage collection을사용해야 한다.
4. 모든 OSG 노드는 reference counted 되어 있어서, reference count가 0으로 줄면 개체를 delete한다.
5. 따라서, OSG의 전체 scene graph를 지우려면 root node 포인터하나만지우면된다.
	![[Pasted image 20240223110422.png]]

## >> osg::Referenced
- 모든 OSG노드와 Scene Graph 데이터 클래스는 `Referenced`에서 파생되어 있다.
- `Referenced` 클래스는 `osg::ref_ptr<>`로 할당할 수 있다.
- `ref_ptr<>` 변수로 `Referenced` 객체를 할당하면 Reference count가 자동적으로 증가한다. 또, `ref_ptr<>` 변수가 scope를 벗어나면 Reference count가 자동적으로 감소한다.
	-> 즉, 살아있는 `ref_ptr` 변수의 개수만큼 `Referenced` 객체의 Reference count가 설정되고, 이 값이 0이되면 `Referenced` 객체의 메모리를 해제한다.(자동 delete)
- **`osg::Referenced` 클래스 의 3가지 주요 기능**
	1. Reference count member variable인 `_refCount`는 클래스 생성자(constructor)에 0으로 초기화 되어있다.
	2. Public methods인 `ref()` 와 `unref()`는 `_refCount` 변수의 증가(incrementing)와 감소 (decrementing)를 담당하고 있다. 그리고, `unref()`는 `_refCount`가 0이 되면 개체를 delete한다.
	3. ==클래스 소멸자(destructor)는 protected 와 virtual이다. 즉, 스택 (stack)에 생성하거나 명시적 파괴(explicit deletion)는 불가능하다.==

## >> osg::ref_ptr
- Referenced 타입 개체의 스마트 포인터 (smart pointer)로 구현되어있다.
- Reference count를 관리한다.
- `Referenced` 개체는 마지막 `ref_ptr<>`가 referencing하고 있는 것이 사라지게 되면 스스로 자신을 delete한다.
- **`osg::ref_ptr`의 주요 기능**
	1. Private 포인터 `_ptr` 은 managed memory address에 저장된다. `get()` 함수를 이용하여 `_ptr` 값을 받는다.
	2. 프로그래머가 `ref_ptr<>`을 일반 C++ 포인터처럼 사용할 수 있도록 `operator->()`나 `operator=()` 같은 다양한 함수를 제공한다.
	3. `ref_ptr<>`이 `NULL`이면 `valid()` 함수는 `false`를 반환한다.
	4. 프로그램에서` ref_ptr<>` 변수로 주소를 할당할 때, `ref_ptr<>` assignment operator인 `operator=()`가 `Referenced::ref()`를 불러서 reference count를 자동적으로 증가시킨다.
	5. `ref_ptr<>`변수가 `Referenced::unref()`를 부르면서 reference count를 감소할 때의 두 가지 경우는 다음과 같다.
		1. 클래스 소멸자에서 `ref_ptr<>` deletion할 때
		2. `operator=()`에서 reassignment할 때

## >> 예제
- `addChild()`하는 경우
	```cpp
	{
	// Create a new osg::Geode object. The assignment to the 
	// osg::ref_ptr<> increments the reference count to 1 
	osg::ref_ptr<osg::Geode> geode = new osg::Geode; 
	// Assume ‘grp’ is a pointer to an osg::Group node. Group uses a 
	// ref_ptr<> to point to its children, so addChild() again increments 
	// the reference count to 2 
	grp->addchild(geode.get());
	} // The ‘geode’ ref_ptr<> variable goes out of scope here. 
	// This decrements the reference count back to 1	
	```
- Referenced 객체를 일반 C++ 포인터로 생성한 경우 (_**명시적 deletion이 안됨에 주의**_)
	```cpp
	osg::Geode geode1 = new osg::Geode; 
	delete geode1; // compile error: destructor is protected
	{ osg::Geode geode2; } // compile error: destructor is protected
	```
	- ==_Referenced 객체를 일반 C++ 포인터로 생성하고 Child에 넣어서 Parent가 Child를 자동으로 delete 하는 방식으로는 삭제 가능_==
		```cpp
		// Create a new osg::Geode object (regular C++ pointer). 
		// Don’t increments the child Geode increment the reference count 1 
		osg::Geode *geode = new osg::Geode;
		// Internal ref_ptr<> in Group increments the child node Geode 
		// reference count to 1 
		grp->addChild(geode);
		```
- Parent가 Scope에서 벗어나서 delete되면서 Child의 refCount가 0이 되어 함께 delete되는 경우
	```cpp
	{
	// ‘top’ increments the Group count to 1 
	osg::ref_ptr<osg::Group> top = new osg::Group; 
	// addChild() increments the Geode count to 1 
	top->addChild(new osg::Geode);
	} // The ‘top’ ref_ptr goes out of scope, deleting both the 
	// Group and Geode memory
	```

## >> 사용 시 주의 사항
- 함수로 개체의 주소를 반환 (Returning the address of an object)할 때 주의해야 한다. 잘못 주소를 반환했을 경우, `ref_ptr<>`가 저장하고 있는 메모리 주소가 반환 스택에 돌려지기 전에 스코프를 벗어나게 된다. ==**아래 예제처럼 쓰면 안됨!!**==
	```cpp
	// Don’t do this. It stores the address as the return value on the call 
	// stack, but when the grp ref_ptr<> goes out of scope, the reference 
	// count goes to zero and the memory is deleted. The calling function 
	// is left with a dangling pointer. 
	osg::Group* createGroup() 
	{ 
		// Allocate a new Group node 
		osg::ref_ptr<osg::Group> grp = new osg::Group; 
		// return the new Group’s address 
		return *grp;
	}
	```
- 위의 문제를 해결하려면 아래와 같이 써야 한다. (`return grp.get()`을 써야함)
	```cpp
	osg::ref_ptr<osg::Group> createGroup() 
	{
	osg::ref_ptr<osg::Group> grp = new osg::Group;
	// return the new Group’s address. This stores the Group address 
	// in a ref_ptr<> and places the ref_ptr<> on the call stack as the 
	// return value 
	return grp.get();
	}
```