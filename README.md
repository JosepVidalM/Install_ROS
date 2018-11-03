# Install_ROS
#Install ROS Melodic en Ubuntu
#lsb_release -a
#Description:	Ubuntu 18.04.1 LTS
#Release:	18.04
#Codename:	bionic
sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu $(lsb_release -sc) main" > /etc/apt/sources.list.d/ros-latest.list'
sudo apt-key adv --keyserver hkp://ha.pool.sks-keyservers.net:80 --recv-key 421C365BD9FF1F717815A3895523BAEEB01FA116
sudo apt update
sudo apt install ros-melodic-desktop-full
sudo rosdep init
rosdep update
sudo rosdep fix-permissions
rosdep update
sudo apt-get install python-rosinstall python-rosinstall-generator python-wstool build-essential
printenv | grep ROS
ROS_ETC_DIR=/opt/ros/melodic/etc/ros
ROS_ROOT=/opt/ros/melodic/share/ros
ROS_MASTER_URI=http://localhost:11311
ROS_VERSION=1
ROS_PYTHON_VERSION=2
ROS_PACKAGE_PATH=/opt/ros/melodic/share
ROSLISP_PACKAGE_DIRECTORIES=
ROS_DISTRO=melodic

source /opt/ros/melodic/setup.bash

Let's create and build a catkin workspace: 
