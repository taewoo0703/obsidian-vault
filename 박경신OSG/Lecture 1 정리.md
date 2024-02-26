# ○ 환경변수
* OSG_FILE_PATH
	* 이미지나 모델을 로딩할때 검색하는 경로
* OSG_NOTIFY_LEVEL
	* 어느정도 수준까지 디버깅 정보를 보여줄지 선택하는 변수 (std::cout으로 보여줌)
	* ALWAYS(least verbose), FATAL, WARN, NOTICE, INFO, DEBUG_INFO, DEBUG_FP(most verbose) 중에 선택 가능
---
# ○ Scene Graph
최상위에 root node를 가지는 그래프 트리 구조
root node는 scene data로 set 함
leaf node는 실제 actual geometry를 포함함
## >> 트리와 씬그래프의 차이점
* 트리 구조는 하나의 자식이 여러 부모를 섬길 수 없다.
* 씬 그래프는 하나의 자식이 여러 부모를 섬길 수 있다.
	*씬 그래프는 하나의 모델노드가 여러개의 transform 노드 부모를 가지면서 씬에 여러개의 모델을 보이게 할 수 있다. 이 방식은 메모리를 절약할 수 있다.  트리 구조는 자식이 여러 부모를 섬길 수 없다*

![[Pasted image 20240220110120.png]]


## >> Rendering Scene Graphs
1. Update (App) traversal
	어플리케이션이 씬그래프를 modify 할 수 있도록 함
2. Cull traversal
	씬에 포함시키기 위해 모든 노드의 bounding volume을 테스트
3. Draw traversal
	cull traversal에서 생성된 geometry들의 리스트를 traverse하고 실제로 렌더링함(low-level graphics API 호출)
4. Event traversal (OSG에서 존재함)
	Update traversal 전에 input이나 다른 이벤트를 처리함

렌더링 순서는 Event 순회 -> Update 순회 -> Cull 순회 -> Draw 순회 이다. 이 순회는 매 프레임마다 시행된다. 스테레오 렌더링이나 다중 디스플레이 환경에서는 Update 순회는 1번하고 각 View마다 Cull 순회와 Draw순회를 실시해야 한다. 

---
# ○ Open Scene Graph
## >> OSG의 특징
* 오픈소스 High Performance 씬그래프 툴킷
	* ANSI C++, STL, OpenGL API로 작성
	* view frustum culling, occlusion culling, small feature culling 지원
	* LOD 기능
	* Vertex arrays, vertex buffer objects
* 멀티 플랫폼 지원
	* 윈도우, 맥, 리눅스, 기타
* 다양한 파일 포맷 지원
	* COLLADA, MAX(.3ds), Performer(.pfb), LightWave (.lwo), Alias Wavefront (.obj), OpenFlight (.flt)
* 다양한 Node Kits
	* Particle system, high quality anti-aliased text, special effects framework, interactive controls

## >> OSG 컴포넌트
* OSG Core
	* 필수 씬그래프 및 렌더링 기능 제공
	* 3D 그래픽 어플리케이션에 필요한 대표적 추가기능 제공
* OSG NodeKits
	* OSG Core 씬 그래프 노드 클래스의 기능을 확장하여 더 높은 수준의 노드 유형 및 특수 효과 제공
* OSG Plugins
	* 2D 이미지, 3D 모델 파일 읽기/쓰기
* 다이어그램
	![[Pasted image 20240220113318.png]]

## >> OSG Libraries
- osg library
	- 벡터, 행렬, geometry, rendering specification and management
	- 3D 응용프로그램을 위한 다른 클래스 such as argument parsing, animation path management, and error and warning communication
- osgUtil library
	- 씬 그래프와 그 콘텐츠에 대한 작업, 통계 수집 및 씬 그래프 최적화, render graph 생성을 위한 클래스와 함수가 포함
- osgDB library
	- 3D DB 생성 및 렌더링을 위한 클래스와 함수가 포함
- osgViewer library
	- 씬에 대한 뷰를 관리하는 클래스를 포함
	- OSG와 다양한 윈도우 시스템 통합

## >> OSG Classes
- osg Library
		- Namespace: osg 
		- Header files /include/osg 
		- Windows library files: osg.dll and osg.lib
	- Node
		모든 노드에 대한 기본 클래스. traversals, culling, application callbacks, state 관리를 용이하도록 하는 메소드를 가지고 있음
	- Group 
		Children을 가질 수 있는 노드에 대한 기본 클래스
	- Geode(Geometry Node)
		OSG의 leaf node에 해당(Children이 없음)
		렌더링할 geometry를 포함하는 osg::Drawable 오브젝트를 포함
	- LOD
		LOD 클래스는 children을 view point와의 거리에 따라서 display
	- MatrixTransform
		자식들의 geometry를 변환시킬 행렬을 가지는 클래스
	- Switch
		자식들을 processing 할지 말지 결정하는 boolean mask를 가지는 클래스

- Geometry classes
	- Drawable 
		geometric data를 저장하는 기본 클래스
	- Geometry
		OpenGL vertex array 기능에 대한 high-level wrapper 역할
	- Primitive Set
		OpenGL vertex array drawing 명령에 대한 high-level 지원을 제공
	- Vector classes
		Vec2, Vec3, etc
	- Array classes
		Vec2Array, Vec3Array, etc

- State Management Classes
	- StateSet
		OSG 는 상태 모음(mode and attributes)을 StateSet 클래스에 저장
		씬 그래프의 모든 osg::Node는 StateSet을 가질 수 있음
	- Modes
		OpenGl의 glEnable() 및 glDisable()과 유사함
		mode는 feature를 끄고 켤 수 있게 해줌(such as lighting, blending, fog)
		osg::StateSet::setMode()를 사용
	- Attributes
		state 파라미터를 저장
		osg::StateSet::setAttribute()를 사용
	- Texture attributes and modes 
		osg::StateSet::setTextureMode() 과 osg::StateSet::setTextureAttribute() 사용

