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

(uvc camera)
$ rosrun uvc_camera uvc_camera_node /image_raw:=/camera/image_raw

(darknet)
$ roslaunch darknet_ros yolo_v3.launch

(object reader)
$ roslaunch object_reader object_reader.launch

(robot controller)
$ rosrun robot_controller robot_controller
```
## Contribution
SDK read_write.cpp  -> ROS package

## Reference
- [uvc_camera](http://wiki.ros.org/uvc_camera/)
- [darknet_ros](https://github.com/leggedrobotics/darknet_ros/)
- [audio_common (sound_play)](https://github.com/ros-drivers/audio_common)
