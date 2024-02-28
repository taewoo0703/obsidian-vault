# ○ 멤버 변수
1. `osg::Light` 선언부
	![[osg_Light 멤버.png]]
	- `_ambient`, `_diffuse`, `_specular` : 0~1, w는 not use(빛은 alpha라는 물리량이 없다)
	- `_position` : w=1 이면 positional light, w=0이면 무한한 위치에서 오는 directional light
	- `_spot_cutoff` : degrees 단위
2. 멤버 변수를 바꾸면 그대로 OpenGL의 파라미터로 세팅해줌
	![[osg_Light_apply.png]]
3. OpenGL 파라미터의 의미 ([glLightfv 함수(Gl.h) - Win32 apps | Microsoft Learn](https://learn.microsoft.com/ko-kr/windows/win32/opengl/gllightfv))
	- **GL_AMBIENT**
			_params_ 매개 변수에는 조명의 앰비언트 RGBA 강도를 지정하는 4개의 부동 소수점 값이 포함됩니다. 부동 소수점 값은 직접 매핑됩니다. 정수나 부동 소수점 값은 고정되지 않습니다. 기본 주변 광원 강도는 (0.0, 0.0, 0.0, 1.0)입니다.
	- **GL_DIFFUSE**
			_params_ 매개 변수에는 광원의 확산 RGBA 강도를 지정하는 4개의 부동 소수점 값이 포함됩니다. 부동 소수점 값은 직접 매핑됩니다. 정수나 부동 소수점 값은 고정되지 않습니다. 기본 확산 강도는 광원 0 이외의 모든 조명에 대해 (0.0, 0.0, 0.0, 1.0)입니다. 빛 0의 기본 확산 강도는 (1.0, 1.0, 1.0, 1.0)입니다.
	- **GL_SPECULAR**
			_params_ 매개 변수에는 조명의 반사 RGBA 강도를 지정하는 4개의 부동 소수점 값이 포함됩니다. 부동 소수점 값은 직접 매핑됩니다. 정수나 부동 소수점 값은 고정되지 않습니다. 기본 반사 강도는 광원 0 이외의 모든 조명에 대해 (0.0, 0.0, 0.0, 1.0)입니다. 빛 0의 기본 반사 강도는 (1.0, 1.0, 1.0, 1.0)입니다.
	- **GL_POSITION**
			_params_ 매개 변수에는 동종 개체 좌표에서 조명의 위치를 지정하는 4개의 부동 소수점 값이 포함됩니다. 정수 및 부동 소수점 값은 모두 직접 매핑됩니다. 정수나 부동 소수점 값은 고정되지 않습니다.  
			**위치는 glLightfv**가 호출될 때(점인 것처럼) modelview 행렬에 의해 변환되고 눈 좌표에 저장됩니다. 위치의 _w_ 구성 요소가 0.0이면 광원이 방향 소스로 처리됩니다. 확산 및 반사 조명 계산은 조명의 방향을 고려하지만 실제 위치는 고려하지 않으며 감쇠는 사용하지 않도록 설정됩니다. 그렇지 않으면 확산 및 반사 조명 계산은 눈 좌표에서 조명의 실제 위치를 기반으로 하며 감쇠가 사용됩니다. 기본 위치는 (0,0,1,0); 따라서 기본 광원은 방향, 병렬 및 -_z_ 축의 방향입니다.
	- **GL_SPOT_DIRECTION**
			_params_ 매개 변수에는 같은 유형의 개체 좌표에서 조명의 방향을 지정하는 세 개의 부동 소수점 값이 포함됩니다. 정수 및 부동 소수점 값은 모두 직접 매핑됩니다. 정수나 부동 소수점 값은 고정되지 않습니다.  
			스폿 방향은 **glLightfv** 가 호출될 때(정상인 것처럼) modelview 행렬의 역방향에 의해 변환되고 눈 좌표에 저장됩니다. GL_SPOT_CUTOFF 기본적으로 180이 아닌 경우에만 중요합니다. 기본 방향은 (0,0,1)입니다.
	- **GL_SPOT_EXPONENT**
			_params_ 매개 변수는 조명의 강도 분포를 지정하는 단일 부동 소수점 값입니다. 정수 및 부동 소수점 값은 직접 매핑됩니다. \[0, 128] 범위의 값만 허용됩니다.  
			유효 광강도는 광원의 방향과 광원에서 조명되는 꼭짓점까지의 방향 사이의 각도의 코사인에 의해 감쇠되고, 스폿 지수의 힘으로 높아집니다. 따라서 스폿 지수가 높을수록 스폿 컷오프 각도에 관계없이 더 집중된 광원이 생성됩니다. 기본 스폿 지수는 0이므로 균일한 조명 분포가 발생합니다.
	- **GL_SPOT_CUTOFF**
			_params_ 매개 변수는 광원의 최대 확산 각도를 지정하는 단일 부동 소수점 값입니다. 정수 및 부동 소수점 값은 직접 매핑됩니다. \[0, 90] 범위의 값과 특수 값 180만 허용됩니다.
			조명 방향과 조명에서 조명되는 꼭짓점까지의 방향 사이의 각도가 스폿 컷오프 각도보다 크면 조명이 완전히 마스킹됩니다. 그렇지 않으면 해당 강도는 스폿 지수 및 감쇠 요인에 의해 제어됩니다. 기본 스폿 컷오프는 180이므로 균일한 조명 분포가 발생합니다.
	- **GL_CONSTANT_ATTENUATION, GL_LINEAR_ATTENUATION, GL_QUADRATIC_ATTENUATION**
			_params_ 매개 변수는 세 가지 광원 감쇠 요소 중 하나를 지정하는 단일 부동 소수점 값입니다. 정수 및 부동 소수점 값은 직접 매핑됩니다. 양수값만 허용됩니다.  
			조명이 방향이 아닌 위치인 경우 해당 강도는 상수 계수, 조명되는 광원과 꼭짓점 사이의 거리를 곱한 선형 계수, 같은 거리의 제곱을 곱한 정사각형의 합에 의해 감쇠됩니다. 기본 감쇠 요소는 (1,0,0)이므로 감쇠가 없습니다.

# ○ 감쇠(Attenuation)
1. Constant Attenuation, Linear Attenuation, Quadratic Attenuation 세 종류가 있다.
	1. 실제 현실은 Quadratic 감쇠이다.(거리의 제곱에 반비례)
	2. 하지만 그래픽에서 Quadratic 100%로 하면 광원 근처만 과하게 밝고 급격하게 어두워지는 현상을 띈다.
	3. 그래서 그래픽에서는 Constant 감쇠와 Linear 감쇠를 섞어서 감쇠가 덜하게 만들어준다. 
2. 참고 : [[opengl].[#2.GLSL] 14. Positional light (tistory.com)](https://learn-and-give.tistory.com/62)
	![[Positional Light 개념.png]]

# ○ spot_exponent(감쇠지수)와 spot_cut_off
1. exponent와 cut_off angle은 spot light에만 적용되는 옵션이다.
	※ *위에서 설명한 (constant, linear, quadratic 감쇠는 점광원에도 적용된다)*
2. cut_off angle은 물리적으로 원뿔 형태의 spot light에 대한 제한 각도를 의미한다.
3. exponent는 조명의 방향에서 멀어질 수록 어두워지는 효과를 내기 위한 계수이다.
	$$spotEffect=(spotDirection*lightDir)^{spotExponent}$$
4. 참고 : [[opengl].[#2.GLSL] 15. Spot light (tistory.com)](https://learn-and-give.tistory.com/63)

# ○ ambient, diffuse, specular
1. ambient light (주변광) : 수많은 반사를 거쳐서 광원이 불분명한 빛이다. 물체를 덮고 있는 빛이며 일정한 밝기와 색으로 표현된다.
2. diffuse light (분산광) : 물체의 표면에서 분산되어 눈으로 바로 들어오는 빛이다. 각도에 따라 밝기가 다르다.
3. specular light (반사광) : 분산광과 달리 한 방향으로 완전히 반사되는 빛이다. 반사되는 부분은 흰색의 광으로 보인다.
4. ![[빛의 종류.png]]
5. osg::Light의 \_ambient, \_diffuse, \_specular는 (r, g, b, w) 형태의 벡터이다.
	w는 아무런 의미 없다. (빛은 alpha가 없다)
6. 참고 1 : [[Learn OpenGL 번역] 3-2. 조명 - 기본 조명 (tistory.com)](https://heinleinsgame.tistory.com/15)
7. 참고 2 : [Introduction to Computer Graphics, Section 4.1 -- Introduction to Lighting (hws.edu)](https://math.hws.edu/graphicsbook/c4/s1.html#gl1light.1.2)
