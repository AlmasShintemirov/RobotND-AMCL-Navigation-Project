# RobotND AMCL Navigation Project
Udacity Robotics Software Engineer Nanodegree Project 3
This project implements ROS Localisation and Navigation using Adaptive Monte Carlo Localisation (ROS AMCL package http://wiki.ros.org/amcl) with a skid-steer robot

Prerequisites
Ubuntu OS 
Robot Operating System (ROS) Kinetic or Melodic

Install ROS nodes required for the local and global planners, amcl, maps and motor control for the navigation stack.
$ sudo apt-get update
$ sudo apt-get install ros-melodic-move-base
$ sudo apt-get install ros-melodic-map-server
$ sudo apt-get install ros-melodic-amcl

Installing
Clone this repository in your catkin workspace 'src/' folder.
$ cd ~/catkin_ws/src/
$ git clone 



For manual robot teleoperation install Teleop Package
f you prefer to control your robot to help it localize itself as you did in the lab, you would need to add the teleop node to your package. Thanks to the ROS community, we could use ros-teleop package to send command to the robot using keyboard or controller.

Clone the ros-teleop package to your src folder:

cd /home/workspace/catkin_ws/src
git clone https://github.com/ros-teleop/teleop_twist_keyboard
Build the package and source the setup script:

cd ..
catkin_make
source devel/setup.bash
Now you could run the teleop script as is described in the README file:

rosrun teleop_twist_keyboard teleop_twist_keyboard.py


Build the project:

$ cd ~/catkin_ws
$ catkin_make
If you haven’t already, the following line can be added to your .bashrc to auto-source all new terminals

source ~/catkin_ws/devel/setup.bash
Run the Code
In a terminal window, type the following,

$ cd ~/catkin_ws
$ roslaunch skid_steer_bot udacity_world.launch
In a new terminal, run the 'amcl.launch' file.

$ cd ~/catkin_ws
$ source devel/setup.bash
$ roslaunch skid_steer_bot amcl.launch
Gazebo and Rviz will load and you should arrive at a result similar to the below.



to run the package 
1) git clone the package into your ../catkin_ws/src folder 
2) cd ../catkin_ws
3) catkin_make
4) source devel/setup.bash
4) roslaunch my_robot world.launch
5) roslaunch ball_chaser ball_chaser.launch
6) rosrun rqt_image_view rqt_image_view 

Environemnt map of the Gazebo world was created using pgm_map_creator package 
https://github.com/udacity/pgm_map_creator
