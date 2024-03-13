mapNode를 가지고 있고, 고도(HAT)에 따라 nearFarRatio를 업데이트 해주는 cullCallback
![[Pasted image 20240313160632.png]]

# ○ 멤버 변수
```cpp
protected:
	bool   _active;
	double _minNearFarRatio, _maxNearFarRatio;
	double _haeThreshold;
	double _rp2, _rp;
	bool   _autoFarPlaneClamping;
	osg::observer_ptr<MapNode> _mapNode;
	PerObjectFastMap< osg::Camera*, 
		osg::ref_ptr<osg::CullSettings::ClampProjectionMatrixCallback> > _clampers;
```
- `_active` : mapNode가 geocentric이면 true
- `_minNearFarRatio` : 고도(HAT)가 0일 때의 near/far 비율
- `_maxNearFarRatio` : 고도(HAT)가 `_haeThreshold` 이상 일 때의 near/far 비율
- `_haeThreshold` : 고도(HAT) threshold
- `_rp` : min(지구 극 반지름, 지구 적도 반지름)
- `_rp2` : `_rp`의 제곱 (=`_rp`^2)
- `_autoFarPlaneClamping` : 기본값은 true
	- true : 수평선(지평선)까지의 거리를 계산하여 Far Plane으로 선정한다.
	- false : double 자료형의 최대값을 Far Plane으로 선정한다.
- `_mapNode` : 생성자에서 넣어주는 mapNode
- `_clampers` : osg::CullSettings::ClampProjectionMatrixCallback을 상속받아 만든 CustomProjClamper를 가지고 있는 맵

# ○ 콜백 함수
- `void AutoClipPlaneCullCallback::operator()( osg::Node* node, osg::NodeVisitor* nv )`
	- traverse할 때 호출되는 콜백함수
	- osg::Camera랑 osgEarth::Map을 기반으로 카메라의 현재 위치(고도)를 파악하고 `_clamper`의 요소,  [[CustomProjClamper]] 인스턴스의 멤버변수를 수정함.
		- `_maxFar`를 지정함.
			- `_autoFarPlaneClamping`가 true 이면 카메라와 수평선(지평선)까지의 거리로 지정
			- `_autoFarPlaneClamping`가 false 이면 DBL_MAX
			- 
		- `_nearFarRatio`를 수정함