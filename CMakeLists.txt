cmake_minimum_required(VERSION 2.8.3)
project(inwheel_motor_controller)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  serial
  std_msgs
)

catkin_package(
  CATKIN_DEPENDS
    serial
    std_msgs
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

add_executable(inwheel_motor_controller_node src/inwheel_motor_controller.cpp)

target_link_libraries(inwheel_motor_controller_node
  ${catkin_LIBRARIES}
)

