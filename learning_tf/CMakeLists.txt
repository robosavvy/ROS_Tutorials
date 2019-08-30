cmake_minimum_required(VERSION 2.8.3)
project(learning_tf)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  tf
  turtlesim
)

catkin_package(

)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

add_executable(turtle_tf_listener_debug src/turtle_tf_listener_debug.cpp)
target_link_libraries(turtle_tf_listener_debug ${catkin_LIBRARIES})