cmake_minimum_required(VERSION 2.8.3)
project(kaqi_msgs)

find_package(catkin REQUIRED COMPONENTS message_generation std_msgs geometry_msgs)

add_message_files(
  FILES
  BatteryState.msg
  ControlBreaker.msg
  BaseParam.msg
)

#add_service_files(
#  FILES
#  SetLaserTrajCmd.srv
#)

generate_messages(DEPENDENCIES geometry_msgs std_msgs)

catkin_package(CATKIN_DEPENDS message_generation std_msgs geometry_msgs)
