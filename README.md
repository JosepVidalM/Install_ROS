## Install_ROS
## Install ROS Melodic en Ubuntu
* lsb_release -a
* Description:	Ubuntu 18.04.1 LTS
* Release:	18.04
* Codename:	bionic
* sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
* sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
* sudo apt update
* sudo apt install ros-melodic-desktop-full
* sudo rosdep init
* rosdep update
* sudo rosdep fix-permissions
* rosdep update
* sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool build-essential
* printenv | grep ROS
* ROS_ETC_DIR=/opt/ros/melodic/etc/ros
* ROS_ROOT=/opt/ros/melodic/share/ros
* ROS_MASTER_URI=http://localhost:11311
* ROS_VERSION=1
* ROS_PYTHON_VERSION=2
* ROS_PACKAGE_PATH=/opt/ros/melodic/share
* ROSLISP_PACKAGE_DIRECTORIES=
* ROS_DISTRO=melodic

* source /opt/ros/melodic/setup.bash

* Let's create and build a catkin workspace: 
* mkdir -p ~/catkin_ws/src
* cd ~/catkin_ws/
* catkin_make
* ls --> build  devel  src
* echo $ROS_PACKAGE_PATH --> /home/youruser/catkin_ws/src:/opt/ros/kinetic/share
* echo $ROS_PACKAGE_PATH --> /opt/ros/melodic/share 
## ERROR????

## Navigating the ROS Filesystem
*sudo apt-get install ros-melodic-ros-tutorials
* rospack find roscpp
* /opt/ros/melodic/share/roscpp
* pwd
* /opt/ros/melodic/share/roscpp
* echo $ROS_PACKAGE_PATH
* /opt/ros/melodic/share

## Creating a ROS Package
* cd ~/catkin_ws
* catkin_make
* . ~/catkin_ws/devel/setup.bash

## Understanding ROS Nodes
* sudo apt-get install ros-melodic-ros-tutorials
* Nodes: A node is an executable that uses ROS to communicate with other nodes.
* Messages: ROS data type used when subscribing or publishing to a topic.
* Topics: Nodes can publish messages to a topic as well as subscribe to a topic to receive messages.
* Master: Name service for ROS (i.e. helps nodes find each other)
* rosout: ROS equivalent of stdout/stderr
* roscore: Master + rosout + parameter server (parameter server will be introduced later) 

roscore
... logging to /home/josep/.ros/log/5e594bd6-e119-11e8-be31-0026bb12c270/roslaunch-josep-MacBookPro-9313.log
Checking log directory for disk usage. This may take awhile.
Press Ctrl-C to interrupt
Done checking log file disk usage. Usage is <1GB.

started roslaunch server http://josep-MacBookPro:44995/
ros_comm version 1.14.3


SUMMARY
========

PARAMETERS
 * /rosdistro: melodic
 * /rosversion: 1.14.3

NODES

auto-starting new master
process[master]: started with pid [9323]
ROS_MASTER_URI=http://josep-MacBookPro:11311/

setting /run_id to 5e594bd6-e119-11e8-be31-0026bb12c270
process[rosout-1]: started with pid [9334]
started core service [/rosout]












