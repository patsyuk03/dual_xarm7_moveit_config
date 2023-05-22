# Dual xArm7 MoveIt configuration package
## Contents
* [1. Introduction](#1-introduction)
* [2. Preparations before using this package](#2-preparations-before-using-this-package)
* [3. Connecting the robot](#3-connecting-the-robot)
* [4. Using dual_xarm7_moveit_config package](#4-using-dual_xarm7_moveit_config-package)
## 1. Introduction
This repository is MoveIt configuration package for the dual xArm 7 manipulator robot with gripper. It was initially generated with MoveIt Setup Assistant and castomised for the use with UFACTORY xArm 7 robot. MoveIt configuration packages [dual_xarm6_moveit_config](https://github.com/xArm-Developer/xarm_ros/tree/master/dual_xarm6_moveit_config) and [xarm7_gripper_moveit_config](https://github.com/xArm-Developer/xarm_ros/tree/master/xarm7_gripper_moveit_config) were taken as a reference.
## 2. Preparations before using this package
### 2.1. Get 'xarm_ros'
Clone xarm_ros repository <https://github.com/xArm-Developer/xarm_ros.git> and go through instractions in README.md
### 2.2. Get 'dual_xarm7_moveit_config'
Clone dual_xarm7_moveit_config to the xarm_ros repository:
```bash
$ cd ~/catkin_ws/src/xarm_ros
$ git clone https://github.com/patsyuk03/dual_xarm7_moveit_config.git
$ cd ~/catkin_ws
$ catkin build
```
## 3. Connecting the robot
Connect two xArm 7 and PC to the WiFi router with ethernet cables (router's network should be 192.168.1.X).
## 4. Using dual_xarm7_moveit_config package
To run MoveIt motion planner to control the real xArm:
```bash
$ roslaunch dual_xarm7_moveit_config realMove_exec.launch robot_ip_1:=<controller box LAN IP address 1> robot_ip_2:=<controller box LAN IP address 2>
```
