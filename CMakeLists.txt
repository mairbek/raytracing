cmake_minimum_required(VERSION 3.10)

project(
  raytracing 
  VERSION 1.0
  LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED True)


# add_library(vec3 vec3.h vec3.cc)

add_library(vec3 INTERFACE)

# 2) Specify where to find the header (usage requirement)
target_include_directories(vec3
    INTERFACE
        $<BUILD_INTERFACE:${CMAKE_CURRENT_SOURCE_DIR}/>
        $<INSTALL_INTERFACE:include>
)

add_executable(raytracing main.cc)
target_link_libraries(raytracing PRIVATE vec3)
