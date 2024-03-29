# YOLO test

## Usage
- Needed Items: Dynamixel 2XL430 x 1, USB video camera x 1, cell phone x 1
- Expected Result: Reponse from the motor and speaker when recognising the phone

### Install ROS Kinetic
```sh
$ sudo apt-get update && sudo apt-get upgrade
$ wget https://raw.githubusercontent.com/rjshim/yolo_test/master/install_ros_kinetic.sh && chmod 755 ./install_ros_kinetic.sh && bash ./install_ros_kinetic.sh
```
### Install ROS packages and Build
```sh
(Move to your catkin workspace)
$ cd ~/catkin_ws/src/

(Download packages)
$ git clone https://github.com/rjshim/yolo_test.git
$ git clone https://github.com/ROBOTIS-GIT/DynamixelSDK.git

(Install binary packages)
$ sudo apt-get install ros-kinetic-uvc-camera
$ sudo apt-get install ros-kinetic-sound-play
$ sudo apt-get install ros-kinetic-darknet-ros-msgs

(Build)
$ cd ~/catkin_ws && catkin_make
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
## Reference
- [uvc_camera](http://wiki.ros.org/uvc_camera/)
- [darknet_ros](https://github.com/leggedrobotics/darknet_ros/)
- [audio_common (sound_play)](https://github.com/ros-drivers/audio_common)
- [DynamixelSDK](https://github.com/ROBOTIS-GIT/DynamixelSDK)
