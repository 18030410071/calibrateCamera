calibrate camera  相机校正，使用opencv自带的函数库，计算出如下几个参数。

内参矩阵： 3*3  
In [22]: mtx  
Out[22]:   
array([[1.16022336e+03, 0.00000000e+00, 6.68285471e+02],  
       [0.00000000e+00, 1.15738493e+03, 3.89459697e+02],  
       [0.00000000e+00, 0.00000000e+00, 1.00000000e+00]])  

畸变矩阵： 1*5  
In [25]: dist  
Out[25]: array([[-0.25129777,  0.02823272, -0.00053603,  0.00037274, -0.08995589]])  
  
  
旋转矩阵:  
In [27]: rvecs  
Out[27]: 18*(3*1)  
[array([[ 0.03558055], [-0.03112721], [-0.00755535]]),   
 array([[ 0.63788424], [-0.04903354], [ 0.01762295]]),   
 array([[-0.44908256], [-0.06512295], [-0.01916963]]),  
 array([[ 0.01780734], [ 0.0209126 ], [-0.00558506]]),   
 array([[0.02198169],  [0.6367404 ],  [0.00977959]]),   
 array([[ 0.03046199], [-0.7040381 ], [-0.01932221]]),   
 array([[-0.19237824], [-0.75952006], [ 0.1201012 ]]),   
 array([[ 0.51440228], [-0.2194547 ], [ 0.02910641]]),   
 array([[0.03761499],  [0.45929723],  [0.00663988]]),   
 array([[0.03691831],  [0.64815823],  [0.01041448]]),   
 array([[-0.3272451 ], [ 0.65900314], [-0.41478724]]),   
 array([[ 0.05770817], [-0.51997066], [-0.00538347]]),   
 array([[-0.01886995], [-0.48934854], [ 0.01885913]]),   
 array([[ 0.04012555], [-0.46639335], [-0.05743551]]),   
 array([[ 0.18608573], [-0.05068572], [-0.00117477]]),   
 array([[ 0.22181091], [-0.06412907], [ 0.0115335 ]]),   
 array([[0.0882598 ],  [0.38487441],  [0.05529661]]),   
 array([[-0.01748482], [ 0.38362373], [-0.00271536]])]  
  

平移向量: 18*(3*1)  
In [33]: tvecs  
Out[33]:   
[array([[-4.21904478], [-2.32362579], [ 8.49747635]]),   
 array([[-3.81963279], [-1.62195346], [ 7.98860175]]),   
 array([[-4.39150219], [-3.07999134], [10.75041784]]),   
 array([[-4.94259067], [-3.93663095], [30.57685167]]),   
 array([[-9.62311687], [-3.36509195], [32.2423649 ]]),   
 array([[ 0.73000489], [-2.96584094], [19.6837078 ]]),   
 array([[-0.85448692], [-4.63545431], [21.80683115]]),   
 array([[-2.09590548], [-0.77674132], [19.65246328]]),   
 array([[-16.99384696],[ -3.57759924],[ 32.14998811]]),   
 array([[-0.19382096], [-3.52948313], [21.95184873]]),   
 array([[-6.04109212], [-1.6349801 ], [26.75950346]]),   
 array([[ 5.40125149], [-4.50757377], [20.8880559 ]]),   
 array([[ 4.51225567], [-1.52138071], [20.08076553]]),   
 array([[ 4.91858056], [-5.1101675 ], [19.89170706]]),   
 array([[-3.63023758], [-4.17313449], [17.87154811]]),   
 array([[-3.96462648], [-1.36057071], [17.1048456 ]]),   
 array([[-13.02067108],[ -5.65276501],[ 23.81054552]]),   
 array([[-13.4309631 ],[ -0.55047404],[ 24.62701854]])]  
   
 
 
通过计算后的参数生成未畸变的图片image.jpg  
