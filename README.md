# GNSS Algorithm based on RTKLIB

![GNSS-Explorer.png](https://github.com/brucezhcw/GNSS-Explorer/blob/VisualStudio/image/GNSS-Explorer.png) 

本项目代码以RTKLIB为基础，用EKF扩展卡尔曼滤波算法实现了低精度绝对观测伪距 + 高精度相对观测多普勒数据的融合。
相对观测多普勒数据精度较高（多普勒速度误差典型值10cm/s），结合卡尔曼滤波算法，可以保证定位轨迹局部的连续性，
绝对观测伪距精度较低，但可以保证全局无偏，二者融合效果非常棒

目前代码维护两个分支对应两个平台：linux + Visual Studio

参考资料：[GNSS算法进阶（二）- kalman滤波单点定位算法代码实现](https://zhuanlan.zhihu.com/p/577601009)
