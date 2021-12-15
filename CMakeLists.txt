cmake_minimum_required(VERSION 3.0.2)
project(grid_example)

find_package(catkin REQUIRED
roscpp
grid_map_core
grid_map_ros
grid_map_msgs
grid_map_visualization
)

catkin_package(
  INCLUDE_DIRS include
  CATKIN_DEPENDS
)


###########
## Build ##
###########
include_directories(
  include
  ${catkin_INCLUDE_DIRS}
  ${EIGEN3_INCLUDE_DIR}
)

add_executable(${PROJECT_NAME}
  src/main.cpp
)

target_link_libraries(
  ${PROJECT_NAME}
  ${catkin_LIBRARIES}
)