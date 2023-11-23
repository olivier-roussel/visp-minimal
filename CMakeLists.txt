cmake_minimum_required(VERSION 3.0)
 
project(visp-minimal)
 
find_package(VISP REQUIRED)
 
add_executable(visp-minimal visp-minimal.cpp)

# Old way: setting include directories and libraries manually
# include_directories(${VISP_INCLUDE_DIRS})
# target_link_libraries(visp-minimal ${VISP_LIBRARIES})

# or modern cmake: using visp cmake targets, but there are many
# Check VISPModules.cmake file for exhaustive list 
target_link_libraries(visp-minimal visp_core visp_gui visp_io)
