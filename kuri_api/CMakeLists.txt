cmake_minimum_required(VERSION 2.8.3)
project(kuri_api)

find_package(catkin REQUIRED COMPONENTS
  message_generation
  roscpp
  rospy
  std_msgs

)
catkin_python_setup()

add_message_files(
  FILES
  Volume.msg
  VolumeButton.msg
)

generate_messages(
  DEPENDENCIES
  std_msgs
  )

catkin_package(
#  INCLUDE_DIRS include
#  LIBRARIES robot_api
  CATKIN_DEPENDS roscpp rospy
)



include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)
