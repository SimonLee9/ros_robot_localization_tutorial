# ros_robot_localization_tutorial
The ROS robot_localization package: a no-hardware-required hands-on tutorial

# Install
cd ~catkin_ws/src

git clone https://github.com/Kapernikov/ros_robot_localization_tutorial.git

catkin_make

# Running
roslaunch robot_localization_demo robot_localization_demo.launch

rosrun turtlesim turtle_teleop_key

# Source Code
## robot_localization_demo.launch
	### turtlesim_node
	### turtle_teleop_key
	### positioning_system_node
	### odometry_node
	### ekf_localization_node, robot_localization_ekf_node_odom
	### ekf_localization_node, robot_localization_ekf_node_map
