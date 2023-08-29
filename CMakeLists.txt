cmake_minimum_required(VERSION 3.0)
 
project(visp-minimal)
 
find_package(VISP REQUIRED)
 
include_directories(${VISP_INCLUDE_DIRS})
 
add_executable(visp-minimal visp-minimal.cpp)
target_link_libraries(visp-minimal ${VISP_LIBRARIES})

