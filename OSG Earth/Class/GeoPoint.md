> [[ECEF 좌표계]]

Geographic 좌표계(Lat, Lon, Alt)를 사용하는 Point
지구타원체의 종류(srs), 고도의 종류(MSL or HAT)가 설정 필요하다.
- 생성자
	- `GeoPoint(const SpatialReference* srs, double x, double y, double z, const AltitudeMode& mode);`
		- srs
			`osgEarth::SpatialReference* srs = osgEarth::SpatialReference::create("wgs84");`
		- x
			longitude w/ degrees
		- y
			latitude with degress
		- z
			altitude with meters
		- mode
			`osgEarth::ALTMODE_ABSOLUTE` : MSL 고도
			`osgEarth::ALTMODE_RELATIVE` : HAT 고도
- ECEF 좌표계  <-> Geographic 좌표계 변환
	- `bool toWorld(osg::Vec3d& out_world) const;` : Geographic -> ECEF 변환
		this의 지점에 대한 ECEF 값을 out_world 벡터에 설정한다.(unit : meters)
		mode가 `osgEarth::ALTMODE_ABSOLUTE`일 때에만 사용 가능
	- `bool fromWorld(const SpatialReference* srs, const osg::Vec3d& world);` : ECEF -> Geographic 변환
		srs와 ECEF 좌표(unit : meters)를 넣어주면 this의 x, y, z가 설정된다.
- 변환 행렬
	- `bool createLocalToWorld( osg::Matrixd& out_local2world ) const;`
		값을 받을 matrix 변수를 input으로 넣어주면 거기에 LocalToWorld 행렬을 저장함. LocalToWorld 행렬은 MatrixTransform의 \_matrix와 같음. 즉 GeoTransform의 \_matrix와 같음
	- `bool createWorldToLocal( osg::Matrixd& out_world2local ) const;`
		LocalToWorld의 inverse

> [[GeoTransform]]