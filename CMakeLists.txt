cmake_minimum_required(VERSION 2.8.3...3.13)
project(gencxx)

find_package(catkin REQUIRED COMPONENTS genmsg)

catkin_package(
  CATKIN_DEPENDS genmsg
  CFG_EXTRAS gencxx-extras.cmake
)

add_subdirectory(scripts)

message(STATUS "Genmsg destination: ${GENMSG_LANGS_DESTINATION}")
file(WRITE ${CATKIN_DEVEL_PREFIX}/${GENMSG_LANGS_DESTINATION}/gencxx "Pure C++")
install(FILES ${CATKIN_DEVEL_PREFIX}/${GENMSG_LANGS_DESTINATION}/gencxx
  DESTINATION ${GENMSG_LANGS_DESTINATION})

catkin_python_setup()
