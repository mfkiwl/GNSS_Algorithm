cmake_minimum_required(VERSION 2.8.3)
project(gnss_algorithm)

set(CMAKE_BUILD_TYPE "Release")
set(CMAKE_CXX_FLAGS "-std=c++11")
#-DEIGEN_USE_MKL_ALL")
set(CMAKE_CXX_FLAGS_RELEASE "-O3 -Wall -g")

include_directories("/usr/include/")
include_directories(${CMAKE_CURRENT_SOURCE_DIR}/src)

aux_source_directory(src SRC_LIST)
aux_source_directory(src/rcv SRC_LIST)

add_executable(gnss_algorithm GNSS_Algorithm.cpp ${SRC_LIST})

target_link_libraries(gnss_algorithm pthread)

