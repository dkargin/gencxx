install(
  FILES msg.hxx.template srv.hxx.template
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION})

catkin_install_python(
  PROGRAMS gen_cxx.py
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION})
