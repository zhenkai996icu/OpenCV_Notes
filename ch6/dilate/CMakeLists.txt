cmake_minimum_required(VERSION 2.6)
project(test)

set(CMAKE_CXX_FLAGS "-std=c++11")

find_package(OpenCV REQUIRED)
include_directories(${OpenCV_INCLUDE_DIRS})

add_executable(test main.cpp)

target_link_libraries(test ${OpenCV_LIBS})

install(TARGETS test RUNTIME DESTINATION bin)
