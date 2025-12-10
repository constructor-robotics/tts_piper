cmake_minimum_required(VERSION 3.0.2)
project(tts_piper)
find_package(catkin REQUIRED COMPONENTS catkin_virtualenv)

catkin_package()

catkin_generate_virtualenv(
  INPUT_REQUIREMENTS requirements.in
)

catkin_install_python(PROGRAMS scripts/tts
  DESTINATION ${CATKIN_PACKAGE_BIN_DESTINATION}
)

install(DIRECTORY data launch
  DESTINATION ${CATKIN_PACKAGE_SHARE_DESTINATION}
)
