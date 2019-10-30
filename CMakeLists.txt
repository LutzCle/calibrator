cmake_minimum_required(VERSION 3.10)
project(Calibrator VERSION 1.0 LANGUAGES C)

if(NOT CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE Release)
endif()

set(CMAKE_CXX_FLAGS_RELEASE "-O3")

find_library(MATH_LIBRARY m)

add_executable(calibrator calibrator.c)
target_link_libraries(calibrator PRIVATE ${MATH_LIBRARY})
