# YOLO test

## Intro

## How to Use

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


https://github.com/ros-perception/image_common
http://wiki.ros.org/image_transport/Tutorials/SubscribingToImages
https://github.com/ApolloAuto/apollo-platform/tree/master/ros/image_common/image_transport/tutorial

