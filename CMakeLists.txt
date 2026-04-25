cmake_minimum_required(VERSION 3.10)
project(clap_z_depth)

set(CMAKE_CXX_STANDARD 17)

# Matthew Style: include directories
include_directories(include)

add_library(${PROJECT_NAME} SHARED src/main.cpp)

# Output as .clap (which is just a renamed .so or .dll)
set_target_properties(${PROJECT_NAME} PROPERTIES PREFIX "" SUFFIX ".clap")
