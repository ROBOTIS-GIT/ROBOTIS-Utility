cmake_minimum_required(VERSION 2.8.3)
project(ros_mpg321_player)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  std_msgs
)

catkin_package(

)

include_directories(
  include
  ${catkin_INCLUDE_DIRS}
)

add_executable(ros_mpg321_player src/ros_mpg321_player.cpp)

add_dependencies(ros_mpg321_player ${${PROJECT_NAME}_EXPORTED_TARGETS} ${catkin_EXPORTED_TARGETS})

target_link_libraries(ros_mpg321_player
  ${catkin_LIBRARIES}
)