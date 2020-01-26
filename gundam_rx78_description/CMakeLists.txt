cmake_minimum_required(VERSION 2.8.3)
project(gundam_rx78_description)

find_package(ament_cmake REQUIRED)

#############
## Install ##
#############
install(DIRECTORY launch meshes scripts urdf
  DESTINATION share/${PROJECT_NAME}
)