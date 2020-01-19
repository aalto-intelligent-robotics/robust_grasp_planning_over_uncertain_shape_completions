cmake_minimum_required(VERSION 2.8.3)
project(scene_completion_msgs)

## Find catkin macros and libraries
## if COMPONENTS list like find_package(catkin REQUIRED COMPONENTS xyz)
## is used, also find other catkin packages
find_package(catkin REQUIRED COMPONENTS sensor_msgs geometry_msgs message_generation shape_msgs actionlib actionlib_msgs)

add_action_files(
   FILES
   CompleteScene.action
   CompletePartialCloud.action
)

add_message_files(
  FILES
  DepthSample.msg
)
## Generate added messages and services with any dependencies listed here
 generate_messages(
   DEPENDENCIES
   actionlib_msgs
   sensor_msgs 
   geometry_msgs
   shape_msgs
   std_msgs
   actionlib_msgs
 )
catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES test
  CATKIN_DEPENDS message_runtime actionlib sensor_msgs geometry_msgs shape_msgs
)


