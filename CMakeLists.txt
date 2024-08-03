cmake_minimum_required(VERSION 3.8)
project(ros2_practice)

find_package(ament_cmake_auto REQUIRED)

ament_auto_find_build_dependencies()

ament_auto_add_executable(listener
  src/listener.cpp
)

ament_auto_add_executable(talker
  src/talker.cpp
)

install(PROGRAMS
  scripts/listener.py
  scripts/talker.py
  DESTINATION lib/${PROJECT_NAME}
)

ament_auto_package(
  INSTALL_TO_SHARE
)
