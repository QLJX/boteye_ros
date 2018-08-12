# boteye_ros
boteye_ros package<br>
基于boteye驱动程序接口写的ros节点,可以将相机返回的图像（未矫正）和IMU数据以topic的形式发布出来。<br>
* /boteye/left/image_color_raw<br>
* /boteye/right/image_color_raw <br>
* /imu/data_raw<br>
## 安装依赖库
* OpenCV (>3.0)<br>
* Glog: sudo apt-get install libgflags-dev<br>
* GFlags: sudo apt-get isntall libgoogle-glog-dev<br>
如果ROS使用的是indigo版本，建议手动安装oepncv3.0版本以上的cv_bridge（[地址](https://github.com/ros-perception/vision_opencv)）<br>
## 编译
    cd boteye_ros
    mkdir build
    cd build
    cmake ..
    make 
    source devel/setup.bash
    rosrun boteye_ros ros_node
