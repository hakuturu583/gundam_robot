cmake_minimum_required(VERSION 3.5.0)
project(gundam_rx78_control)

find_package(ament_cmake REQUIRED)
find_package(controller_interface REQUIRED)
find_package(ros_controllers REQUIRED)
find_package(pluginlib REQUIRED)

###########
## Build ##
###########
include_directories(include ${pluginlib_INCLUDE_DIRS})

#add_library(${PROJECT_NAME}
#  src/joint_trajectory_controller.cpp
#)

#target_link_libraries(${PROJECT_NAME} ${catkin_LIBRARIES})

#############
## Install ##
#############
install(DIRECTORY config launch sample
  DESTINATION share/${PROJECT_NAME}
)

#install(TARGETS ${PROJECT_NAME}
#  ARCHIVE DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
#  LIBRARY DESTINATION ${CATKIN_PACKAGE_LIB_DESTINATION}
#  RUNTIME DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
#  )


#install(FILES joint_trajectory_controller.xml
#  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})
ament_package()