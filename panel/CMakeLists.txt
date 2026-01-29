cmake_minimum_required(VERSION 3.0.2)
project(panel)

## Compile as C++11, supported in ROS Kinetic and newer
# add_compile_options(-std=c++11)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS
  robot_state_publisher
  roscpp
  rospy
  sensor_msgs
  std_msgs
  tf
)


###########
## Build ##
###########

## Specify additional locations of header files
## Your package locations should be listed before other locations
include_directories(
# include
  ${catkin_INCLUDE_DIRS}
)

add_executable(mainPanel src/main.cpp src/generacionTrayectorias.cpp)
target_link_libraries(mainPanel ${catkin_LIBRARIES})


