cmake_minimum_required(VERSION 3.0.2)
project(mh5_msgs)

find_package(catkin REQUIRED COMPONENTS
  std_srvs
  std_msgs
  message_generation
)

add_message_files(
  FILES
  DeviceStatus.msg
)

add_service_files(
  FILES
  ActivateJoint.srv
)

generate_messages(
  DEPENDENCIES
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS std_msgs message_runtime
)
