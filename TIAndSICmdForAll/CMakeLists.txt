# CMake requirement for minimum version
cmake_minimum_required (VERSION 2.8)

# project information
project (TIAndSICmdForAll)

aux_source_directory(. DIR_SRCS)

set (PROJECT_SOURCE_DIR ${CMAKE_CURRENT_SOURCE_DIR})

set (PROJECT_SOURCE_FILES
  ${PROJECT_SOURCE_DIR}/TIandSIcmd.cpp
  ${PROJECT_SOURCE_DIR}/XGetopt.cpp
  )

include_directories (/usr/local/include)
link_directories(/usr/local/lib)

add_executable (tisi ${PROJECT_SOURCE_FILES})

#target_link_libraries(RISE libopencv_core.so libopencv_imgcodecs.so libopencv_imgproc.so libopencv_highgui.so)
