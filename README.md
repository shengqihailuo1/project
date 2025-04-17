| 项目名称 | 项目描述                                                     | 实现效果                                                     | 项目链接                                                     |
| :------: | :----------------------------------------------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ |
| 时间同步 | 以STM32为时钟源，采用PPS+GPRMC同步Livox激光雷达时间戳，并通过PWM信号同步海康相机时间戳。实现了三种同步方案，解决了Livox驱动的imu时间戳回退、触发信号时序、相机曝光时间补偿等问题。 | 在20FPS图像、10HZ点云的情况下标定出的同步误差从94ms降低到14ms，增强了传感器数据融合的准确性。 | https://github.com/shengqihailuo1/Time_Synchronization       |
| 数据传输 | 开发海康工业相机ROS2驱动，基于FastDDS实现多传输通道架构，为不同场景提供ROS2话题接口或DDS两种通信模式。 | 在50FPS、193MB/s吞吐量场景下，通过零拷贝技术将端到端延迟优化至87μs（较传统方案降低94%）。 | 链接1： https://github.com/shengqihailuo1/HikRobot_Camera_ROS2 <br />链接2：https://github.com/shengqihailuo1/fastDDS_image |
| 目标检测 | 通过融合Swim Transformer等多种Tricks改进YOLO网络的特征提取和融合效果，同时，开发C++ QT交互界面实时展示效果。 | 实验结果mAP指标提高 2.3%，推理速度达到35FPS。                | https://github.com/shengqihailuo1/Object_detection           |

