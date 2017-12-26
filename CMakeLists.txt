# toplevel CMakeLists.txt for a catkin workspace
# catkin/cmake/toplevel.cmake

cmake_minimum_required(VERSION 2.8.3)

include(cmake/HunterGate.cmake)
HunterGate(
    URL "https://github.com/lsolanka/hunter/archive/v0.19.210-7.tar.gz"
    SHA1 "ef27d99536c8b62413dba3ffa19ccd6d25d95f7a"
)

project(ros)
hunter_add_package(Boost COMPONENTS thread)
hunter_add_package(ros-catkin)
hunter_add_package(ros-rospack)

add_subdirectory(core/rosbuild)
add_subdirectory(core/roslang)
add_subdirectory(core/roslib)
add_subdirectory(ros)
add_subdirectory(tools/rosbash)
add_subdirectory(tools/rosboost_cfg)
add_subdirectory(tools/rosclean)
add_subdirectory(tools/roscreate)
add_subdirectory(tools/rosmake)
add_subdirectory(tools/rosunit)
