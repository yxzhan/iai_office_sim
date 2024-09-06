cmake_minimum_required(VERSION 3.5)
project(iai_office_sim)

# Enable C++11 (or later, if desired)
set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Find dependencies
find_package(ament_cmake REQUIRED)
find_package(gazebo_ros REQUIRED)
find_package(PkgConfig REQUIRED)

install(DIRECTORY launch maps models resource worlds rviz
  DESTINATION share/${PROJECT_NAME}/
)

ament_export_dependencies(gazebo_ros)
ament_export_dependencies(PkgConfig)
ament_package()
