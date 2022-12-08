# ros_robot_localization_tutorial
The ROS robot_localization package: a no-hardware-required hands-on tutorial

# Install
cd ~catkin_ws/src

git clone https://github.com/Kapernikov/ros_robot_localization_tutorial.git

catkin_make

# Running
roslaunch robot_localization_demo robot_localization_demo.launch

rosrun turtlesim turtle_teleop_key
