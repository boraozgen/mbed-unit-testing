cmake_minimum_required(VERSION 3.0.0)
project(test)

add_library(mbed-core INTERFACE)

include(mbed_includes.cmake)
target_include_directories(mbed-core INTERFACE ${MBED_INCLUDES})

add_executable(test test.cpp)
target_link_libraries(test mbed-core)