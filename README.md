# ros_robot_localization_tutorial
The ROS robot_localization package: a no-hardware-required hands-on tutorial

# Install
cd ~catkin_ws/src

git clone https://github.com/Kapernikov/ros_robot_localization_tutorial.git

catkin_make

# Running

roslaunch
 
  roslaunch robot_localization_demo robot_localization_demo.launch


rosrun
 
  rosrun turtlesim turtle_teleop_key

# Source Code
## robot_localization_demo.launch
 -  turtlesim_node
 -  turtle_teleop_key
 -  positioning_system_node
 -  odometry_node
 -  ekf_localization_node, robot_localization_ekf_node_odom
 -  ekf_localization_node, robot_localization_ekf_node_map

## 거북이
- 두꺼운 회색선 - 실제 turtlesim 로봇
- 파란색선 - 위치 센서: 거북이의 절대 위치와 방향 측정
- 빨간색선 - 속도 센서: 거북이의 선형 및 각속도 측정
- 두꺼운 녹색 - 맵 프레임에서 거북이 자세에 대한 robots_location 추정치


## 가상의 센서

*include/robot_localization/**positioning_system**.hpp &* src */sensors/**positioning_system**.cpp*
: 위치 센서 클래스 구현


*src/sensors/**positioning_system_node**.cpp*
: 센서의 노드 시작


위치센서

: *turtle1/pose (*topic) → *turtlesim/*Pose (messages)
: *turtle1/sensors/pose (*topic) → sending *geometry_msgs/PoseWithCovarianceStamped (*messages)
