cmake_minimum_required(VERSION 3.5.0)
project(gundam_rx78_control)

find_package(ament_cmake REQUIRED)

#############
## Install ##
#############
install(DIRECTORY config launch sample
  DESTINATION share/${PROJECT_NAME}
)

ament_package()