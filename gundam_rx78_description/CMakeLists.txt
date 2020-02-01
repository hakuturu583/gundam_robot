cmake_minimum_required(VERSION 3.5.0)
project(gundam_rx78_description)

find_package(ament_cmake REQUIRED)

#############
## Install ##
#############
install(DIRECTORY launch meshes scripts urdf
  DESTINATION share/${PROJECT_NAME}
)

ament_package()