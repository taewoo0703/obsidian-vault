- [[code_MatrixTransform]]
- `void setMatrix(const Matrix& mat)` :  변환 행렬을 Set하는 메소드
- `_matrix` : setMatrix를 통해 세팅한 변환 행렬. 
	LocalToWorld 행렬([[좌표변환]])과 같다. 
	[[Affine 변환]] 행렬 (4 x 4)이다.
- preMult 계열 메소드
	1. input이 matrix인 경우
		input을 `_matrix`의 앞에 곱하고 나온 결과를 `_matrix`에 저장함.
		`_matrix = input * _matrix`
	2. input이 quat인 경우
		input을 이용해 회전 변환을 만들고, 그 변환으로 preMult 수행
		`_matrix = rotation_by_quat * _matrix`
	3. input이 vector인 경우
		input을 행벡터로 가정하고, 벡터 * 행렬 연산을 수행한 뒤 나온 값을 return
		`return input * _matrix`
- postMult 계열 메소드(==주의!==)
	1. input이 matrix인 경우
		input을 `_matrix`의 뒤에 곱하고 나온 결과를 `_matrix`에 저장함.
		`_matrix = _matrix * input`
	2. input이 quat인 경우
		input을 이용해 회전 변환을 만들고, 그 변환으로 postMult 수행
		`_matrix = _matrix * rotation_by_quat`
	3. input이 vector인 경우(==주의!==)
		input을 ==**열벡터**==로 가정하고, ==행렬 * 벡터== 연산을 수행한 뒤 나온 값을 return
		`return _matrix * input`
	