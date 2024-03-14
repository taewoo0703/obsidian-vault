osg::CullVisitor에서 카피한 clampProjectionMatrix 메소드를 활용하여 ProjectionMatrix를 변경해주는 클래스

# ○ 멤버 변수
-  `_minNear`, `_maxFar`, `_nearFarRatio` : double

# ○ 멤버 함수
- **clampProjectionMatrixImplementation**
	- `bool clampProjectionMatrixImplementation(osg::Matrixf& projection, double& znear, double& zfar)`
	- input으로 받은 znear, zfar를 내부적으로 가지고 있는 `_minNear`와 `_maxFar`랑 비교하여 범위안에 들어오게 만든 다음 `_clampProjectionMatrix` 함수 호출
- **\_clampProjectionMatrix**
	- `bool _clampProjectionMatrix(matrix_type& projection, double& znear, double& zfar, value_type nearFarRatio)`
	- osg의 clampProjectionMatrix함수를 Wrapping (완벽히 동일하게 복사)
	- 소스 코드 : [[code_clampProjectionMatrix]]
	- 