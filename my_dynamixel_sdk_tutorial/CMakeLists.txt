cmake_minimum_required(VERSION 2.8.3)
project(my_dynamixel_sdk_tutorial)

## Compile as C++11, supported in ROS Kinetic and newer
add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  roscpp
  sensor_msgs
  dynamixel_sdk
)

catkin_package(
  CATKIN_DEPENDS roscpp sensor_msgs dynamixel_sdk
)

include_directories(
 include 
 ${catkin_INCLUDE_DIRS}
)

add_executable(${PROJECT_NAME}_node src/read_write.cpp)
add_dependencies(${PROJECT_NAME}_node ${${PROJECT_NAME}_EXPORTED_TARGETS} ${catkin_EXPORTED_TARGETS})
target_link_libraries(${PROJECT_NAME}_node ${catkin_LIBRARIES})

