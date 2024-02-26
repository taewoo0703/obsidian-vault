# 멤버변수
- **GEODETIC_POSITION** \_position
	- [[GEODETIC_POSITION.png]]
- **PLAYER_POSITION** \_attitude
	- [[PLAYER_ATTITUDE.png]]
- **float** \_heading, \_pitch, \_roll
	*_heading, _pitch, _roll은 host로부터 업데이트 받고, 나중에 CameraControl::UpdateCamera 메소드에서 _attitude를 _heading, _pitch, _roll을 이용하여 업데이트 시켜준다. 변수 중복이라고 생각됨*