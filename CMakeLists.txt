cmake_minimum_required(VERSION 3.10)

project(
  raytracing 
  VERSION 1.0
  LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)


# add_library(mylib my_lib.cpp my_lib.hpp)
add_executable(raytracing main.cc)
# target_link_libraries(main PRIVATE mylib)
