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


Installation

Clone this repository in your catkin workspace 'src/' folder.

$ cd ~/catkin_ws/src/

$ git clone https://github.com/AlmasShintemirov/RobotND-AMCL-Navigation-Project.git


If you prefer to control your robot to help it localize itself as you did in the lab, you would need to add the teleop node to your package. 
Clone the ROS-Teleop package to your src folder:

cd /home/workspace/catkin_ws/src

git clone https://github.com/ros-teleop/teleop_twist_keyboard


Build the package and source the setup script:

cd ..

catkin_make

source devel/setup.bash


To run the project:

roslaunch my_robot_localization world.launch

roslaunch my_robot_localization amcl.launch (in a new terminal window)


For running the robot teleopation:
rosrun teleop_twist_keyboard teleop_twist_keyboard.py (in a new terminal window)

Gazebo and Rviz will load and you should arrive at a result similar to the below.

![position_1](https://user-images.githubusercontent.com/13367696/131977826-a0ba5910-40e6-4ee6-ac9d-c99b854992f3.png)
![position_2](https://user-images.githubusercontent.com/13367696/131977836-e67bc6ff-13b5-426c-890f-5603137fd3a1.png)
![position_3](https://user-images.githubusercontent.com/13367696/131977844-1dd76709-ff71-482c-a362-5162ad9edfc0.png)
![position_4](https://user-images.githubusercontent.com/13367696/131977855-854870a9-1c52-4e46-8bc2-ddc838b90ffe.png)

Environemnt map of the Gazebo world was created using pgm_map_creator package 
https://github.com/udacity/pgm_map_creator
