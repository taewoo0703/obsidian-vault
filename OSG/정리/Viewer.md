# ○ Model, View, Projection Matrix
- model matrix : ModelToWorld 역할
	- v_world = v_model  * modelMatrix
- view matrix : WorldToCamera 역할
	- v_camera = v_world * viewMatrix
- projection matrix : CameraTo2DPlane 역할
	- v_2DPlane = v_camera * projection matrix

# ○ Projection Matrix
- 좌표계 : OpenGL 좌표계를 따른다?? 
	- x : right, y : up, z : backward(화면에서 나오는 쪽)
- Projection Matrix는 Camera 좌표계의 점을 2D평면 상의 점으로 맵핑해주는 역할을한다.
	1. 관측공간(view volume)을 정규관측공간(canonical view volume)으로 맵핑
	2. 정규관측공간을 2D 평면으로 맵핑 (직교투영 방식)
- 정규 관측공간
	- 원점을 중심으로 하고, 길이가 2인 정육면체
	- (-1, -1, -1) 부터 (1, 1, 1) 까지

## >> 직교 투영
- 일반적인 케이스
	![[Pasted image 20240314103204.png]]
	$$P_{general} = TSM_{ortho}$$
- T 행렬
	- 지정된 관측공간의 중심을 정규관측공간의 중심으로 이동
		$$T(\frac{-(left + right)}{2}, \frac{-(top+bottom)}{2}, \frac{-(-far-near)}{2})$$
- S 행렬
	- 지정된 관측공간의 변을 길이가 2가 되도록 크기 변환
	$$S(\frac{2}{right-left}, \frac{2}{bottom-top}, \frac{2}{-far-(-near)})$$
- M 행렬
	- z 평면으로 투영
	- p_view = \[x, y, z, 1] -> q = \[x, y, 0, 1]
	$$M_{ortho} = \begin{bmatrix} 
	1 & 0 & 0 & 0 \\ 
	0 & 1 & 0 & 0 \\
	0 & 0 & 0 & 0 \\
	0 & 0 & 0 & 1
	\end{bmatrix} $$
- Projection Matrix
	- P = T * S로 표현한다.
	- T * S는 관측 공간을 ==Clipping==하여 정규관측공간으로 변환하는 의미
		$$P = TS = \begin{bmatrix} 
		\frac{2}{right-left} & 0 & 0 & 0 \\ 
		0 & \frac{2}{top-bottom} & 0 & 0 \\
		0 & 0 & -\frac{2}{far-near} & 0 \\
		-\frac{right+left}{right-left} & -\frac{top+bottom}{top-bottom} & -\frac{far+near}{far-near} & 1
		\end{bmatrix} $$
	- M_ortho는 ==공간상의 점을 평면상의 점==으로 변환하는 의미 

## >> 원근/투시 투영(미완성)
- 일반적인 케이스
	![[Pasted image 20240314104933.png]]
	$$P_{general} = H(\theta , \phi)STM_{ortho}$$
- H 행렬
	- xy shear (z value unchanged)
		$$H(\theta,\phi) = \begin{bmatrix} 
		1 & 0 & 0 & 0 \\ 
		0 & 1 & 0 & 0 \\
		-cot(\theta) & -cot(\phi) & 1 & 0 \\
		0 & 0 & 0 & 1
		\end{bmatrix} $$
- 원근/투시 투영
	- w/o clipping
		- z=d 인 평면으로 투영
		- p_view = \[x, y, z, 1] -> q = \[x, y, z, z/d] ( = \[xd/z, yd/z, d, 1] )
		$$M_{pers} = \begin{bmatrix} 
		1 & 0 & 0 & 0 \\ 
		0 & 1 & 0 & 0 \\
		0 & 0 & 1 & 1/d \\
		0 & 0 & 0 & 0
		\end{bmatrix} $$
