This project involves designing and simulating a mobile robot capable of moving spheres into a designated 'pen' within a simulation environment provided in assessment_world. The project requires the development of a Universal Robot Description Format (URDF) file for the robot, integration into a Gazebo simulation, and interaction with objects in the environment to complete the assigned task. The project is developed on Ubuntu 20.04 using ROS (Robot Operating System).

Repository Details

Git Repository Link: https://github.com/shalaby2512/PDE4430_CW2

The repository includes:

URDF files for the robot model.


Getting Started

Prerequisites

Ensure the following software is installed on your system:

Ubuntu 20.04

ROS Noetic

Gazebo (compatible with ROS Noetic)

Git

Python 3

Cloning the Repository
git clone https://github.com/shalaby2512/PDE4430_CW2
cd [repository-folder]

Installation

Install ROS Dependencies:
sudo apt update
sudo apt install ros-noetic-desktop-full
sudo apt install ros-noetic-xacro
sudo apt install ros-noetic-joint-state-publisher-gui
sudo apt install ros-noetic-teleop-twist-keyboard

Setup the Workspace:
mkdir -p ~/catkin_ws/src
cd ~/catkin_ws/src
ln -s [repository-folder] ./
cd ~/catkin_ws
catkin_make
source devel/setup.bash

Install Additional Dependencies (if any):
rosdep install --from-paths src --ignore-src -r -y

Launching the Simulation

Start Gazebo with the Simulation Environment:
roslaunch [package-name] assessment_world.launch

Control the Robot:
Use teleoperation or run the provided control nodes.

Approach

The project follows a structured approach:

Robot Design:

A simple robot is designed in the URDF file with essential components: wheels, chassis, and sensors.

Interaction:

ROS nodes handle robot control and interaction with the spheres.

Control:

Teleoperation implemented using teleop_twist_keyboard.

Basic autonomous movement features developed for efficient navigation.

Simulation:

The robot is tested in Gazebo to ensure it can move the spheres to the pen.
