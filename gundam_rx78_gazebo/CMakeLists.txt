cmake_minimum_required(VERSION 3.5.0)
project(gundam_rx78_gazebo)

find_package(ament_cmake REQUIRED)

#############
## Install ##
#############
install(DIRECTORY launch worlds test
  DESTINATION share/${PROJECT_NAME}/
  USE_SOURCE_PERMISSIONS
)

ament_package()