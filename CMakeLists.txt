# This CMakeLists.txt file is only configured for debugging
SET (BOOST_ROOT "C:/Program Files/JetBrains/CLion 2019.2.4/lib/boost_1_71_0")
SET (BOOST_INCLUDEDIR "${BOOST_ROOT}/boost")

SET(Boost_DEBUG ON)


cmake_minimum_required(VERSION 3.6)
project(NOT_ENGLISH)

add_definitions(-std=c++11 -g -Wall)

# For boost:
find_package(Boost 1.54 REQUIRED)
# link_directories(${Boost_LIBRARY_DIRS})
include_directories(${Boost_INCLUDE_DIRS})

set(target_file NOT_ENGLISH)
file(GLOB sources *.cpp)
add_executable(${target_file} ${sources})
cmake_policy(SET CMP0037 NEW)


