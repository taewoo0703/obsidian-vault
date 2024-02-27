# ○ 멤버변수
![[Pasted image 20240227161354.png]]

# ○ 감쇠(Attenuation)
1. Constant Attenuation, Linear Attenuation, Quadratic Attenuation 세 종류가 있다.
	1. 실제 현실은 Quadratic 감쇠이다.(거리의 제곱에 반비례)
	2. 하지만 그래픽에서 Quadratic 100%로 하면 광원 근처만 과하게 밝고 급격하게 어두워지는 현상을 띈다.
	3. 그래서 그래픽에서는 Constant 감쇠와 Linear 감쇠를 섞어서 감쇠가 덜하게 만들어준다. 
2. 참고 : [[opengl].[#2.GLSL] 14. Positional light (tistory.com)](https://learn-and-give.tistory.com/62)
	![[Pasted image 20240227160545.png]]
3. osg::Light 에서는 

# ○ exponent(감쇠지수)와 cut_off
1. ㅇ림ㅇㄹ
2. 참고 : [[opengl].[#2.GLSL] 15. Spot light (tistory.com)](https://learn-and-give.tistory.com/63)
	
1. 