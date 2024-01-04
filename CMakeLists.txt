set_property(GLOBAL PROPERTY TARGET_SUPPORTS_SHARED_LIBS TRUE)

include(/opt/pylon/share/pylon/cmake/genicam-targets.cmake)
include(/opt/pylon/share/pylon/cmake/pylon-targets.cmake)


cmake_minimum_required(VERSION 3.27)
project(pylong_test)
find_package(pylon 7.4.0 REQUIRED)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_FIND_DEBUG_MODE ON)

add_executable(pylong_test main.cpp)

target_link_libraries(pylong_test pylon::pylon)
