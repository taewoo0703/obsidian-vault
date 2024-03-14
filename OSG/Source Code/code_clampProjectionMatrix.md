- CullSettings 파일에 있음.
- 이미 left, right, top, bottom까지는 적용된 projection 행렬에 near, far를 넣어서 projection 행렬 및 znear, zfar를 업데이트 해주는 함수
	- zfar는 zfar보다 미세하게 높은 값으로 바꿔준다.(2% 정도)
	- znear는 znear보다 미세하게 낮은 값으로 바꿔준다.
	- zfar를 기준으로 nearFarRatio를 써서 얻은 값은 znear의 최소 threshold 역할을 한다.
	- 이렇게 정한 znear와 zfar를 기준으로 projection행렬에 nearFarClipping을 해준다.

```cpp
bool clampProjectionMatrix(matrix_type& projection, double& znear, double& zfar, value_type nearFarRatio)
{
    double epsilon = 1e-6;
    if (zfar<znear-epsilon)
    {
        if (zfar != -FLT_MAX || znear != FLT_MAX)
        {
            OSG_INFO<<"_clampProjectionMatrix not applied, invalid depth range, znear = "<<znear<<"  zfar = "<<zfar<<std::endl;
        }
        return false;
    }
    
    if (zfar<znear+epsilon)
    {
        // znear and zfar are too close together and could cause divide by zero problems
        // late on in the clamping code, so move the znear and zfar apart.
        double average = (znear+zfar)*0.5;
        znear = average-epsilon;
        zfar = average+epsilon;
        // OSG_INFO << "_clampProjectionMatrix widening znear and zfar to "<<znear<<" "<<zfar<<std::endl;
    }
    if (fabs(projection(0,3))<epsilon  && fabs(projection(1,3))<epsilon  && fabs(projection(2,3))<epsilon )
    {
        // OSG_INFO << "Orthographic matrix before clamping"<<projection<<std::endl;
        value_type delta_span = (zfar-znear)*0.02;
        if (delta_span<1.0) delta_span = 1.0;
        value_type desired_znear = znear - delta_span;
        value_type desired_zfar = zfar + delta_span;
  
        // assign the clamped values back to the computed values.
        znear = desired_znear;
        zfar = desired_zfar;
  
        projection(2,2)=-2.0f/(desired_zfar-desired_znear);
        projection(3,2)=-(desired_zfar+desired_znear)/(desired_zfar-desired_znear);
  
        // OSG_INFO << "Orthographic matrix after clamping "<<projection<<std::endl;
    }
    else
    {
  
        // OSG_INFO << "Persepective matrix before clamping"<<projection<<std::endl;
  
        //std::cout << "_computed_znear"<<_computed_znear<<std::endl;
        //std::cout << "_computed_zfar"<<_computed_zfar<<std::endl;

        value_type zfarPushRatio = 1.02;
        value_type znearPullRatio = 0.98;
  
        //znearPullRatio = 0.99;

        value_type desired_znear = znear * znearPullRatio;
        value_type desired_zfar = zfar * zfarPushRatio;
  
        // near plane clamping.
        double min_near_plane = zfar*nearFarRatio;
        if (desired_znear<min_near_plane) desired_znear=min_near_plane;

        // assign the clamped values back to the computed values.
        znear = desired_znear;
        zfar = desired_zfar;

        value_type trans_near_plane = (-desired_znear*projection(2,2)+projection(3,2))/(-desired_znear*projection(2,3)+projection(3,3));
        value_type trans_far_plane = (-desired_zfar*projection(2,2)+projection(3,2))/(-desired_zfar*projection(2,3)+projection(3,3));
  
        value_type ratio = fabs(2.0/(trans_near_plane-trans_far_plane));
        value_type center = -(trans_near_plane+trans_far_plane)/2.0;
  
        projection.postMult(osg::Matrix(1.0f,0.0f,0.0f,0.0f,
                                        0.0f,1.0f,0.0f,0.0f,
                                        0.0f,0.0f,ratio,0.0f,
                                        0.0f,0.0f,center*ratio,1.0f));

        // OSG_INFO << "Persepective matrix after clamping"<<projection<<std::endl;
    }
    return true;
}
```