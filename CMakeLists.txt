cmake_minimum_required(VERSION 3.0.2)
project(com_world)

add_compile_options(-std=c++11)

find_package(catkin REQUIRED COMPONENTS
  roscpp
  rospy
  std_msgs
  geometry_msgs
  sensor_msgs
  nav_msgs
  tf
  tf2_ros
  gazebo_ros
  xacro
  turtlebot3_description
  map_server
  amcl
  robot_state_publisher
  joint_state_publisher
  message_runtime
)

catkin_package(
  CATKIN_DEPENDS
    rospy
    std_msgs
    geometry_msgs
    sensor_msgs
    nav_msgs
    tf
    tf2_ros
)

include_directories(
  ${catkin_INCLUDE_DIRS}
)

# === INSTALL DIRECTORIES ===
install(DIRECTORY launch/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/launch)

install(DIRECTORY world/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/world)

install(DIRECTORY maps/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/maps)

install(DIRECTORY urdf/
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}/urdf)

# === INSTALL PYTHON SCRIPTS ===
catkin_install_python(PROGRAMS
  scripts/global_planner.py
  scripts/kinematic_controller.py
  scripts/potential_field.py
  scripts/navigator.py         
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

