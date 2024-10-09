cmake_minimum_required(VERSION 3.22)

project(batched_BLAS
  VERSION 0.0.0
  LANGUAGES C CXX)

set(CMAKE_C_STANDARD 11)
set(CMAKE_CXX_STANDARD 11)

option(BUILD_SHARED_LIBS "Build shared or static library" OFF)
option(INTEGER_SIZE      "Integer size in bytes"          8)

set(SOURCES)

add_subdirectory(src)

add_library(batched_blas ${SOURCES})
