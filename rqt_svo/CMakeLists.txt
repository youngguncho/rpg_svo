cmake_minimum_required(VERSION 2.8.3)
project(rqt_svo)
#set (CMAKE_PREFIX_PATH /opt/Qt5.6.1/5.6/gcc_64/lib/cmake)
find_package(catkin REQUIRED COMPONENTS
  rospy
  rqt_gui
  rqt_gui_py
)
catkin_package()
catkin_python_setup()

install(FILES plugin.xml
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(DIRECTORY resource
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)

install(PROGRAMS scripts/rqt_svo
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)
