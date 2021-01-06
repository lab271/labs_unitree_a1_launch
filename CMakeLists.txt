cmake_minimum_required(VERSION 2.8.3)
project(labs_unitree_a1_launch)

add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
   # controller_manager
    roscpp
    unitree_legged_base_controller
    move_base
    
)

find_package(Eigen3 REQUIRED)

catkin_package(
 )

include_directories(
    include
    ${catkin_INCLUDE_DIRS}
)

install(DIRECTORY launch params maps
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)



