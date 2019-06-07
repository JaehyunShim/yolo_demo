# YOLO test

## Intro

## How to Use

### Install ROS Kinetic
```sh
$ sudo apt-get update && sudo apt-get upgrade
$ wget https://raw.githubusercontent.com/RyanJaehyunShim/git_test/master/install_ros_kinetic.sh && chmod 755 ./install_ros_kinetic.sh && bash ./install_ros_kinetic.sh
```
### Install ROS packages
```sh
(Move to your catkin workspace)
$ cd ~/catkin_ws/src/

(Download packages)
$ git clone https://github.com/ROBOTIS-GIT/DynamixelSDK.git

(Download packages)
$ sudo apt-get install ros-kinetic-uvc-camera
```

### Execute ROS packages
```sh
$ roscore
$ rosrun uvc_camera uvc_camera_node /image_raw:=/camera/image_raw
$ roslaunch darknet_ros yolo_v3.launch
$ rosrun sound_play soundplay_node.py
$ rosrun sound_play test
$ rosrun robot_controller robot_controller
```

## Contribution
SDK read_write.cpp  -> ROS package

## Reference
- [darknet_ros](https://github.com/leggedrobotics/darknet_ros/)
- [audio_common](https://github.com/ros-drivers/audio_common)
