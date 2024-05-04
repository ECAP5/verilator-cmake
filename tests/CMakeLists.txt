cmake_minimum_required(VERSION 3.12)

project(verilator-cmake-test VERSION 1.0)

include(${CMAKE_CURRENT_LIST_DIR}/../cmake/verilator-config.cmake)

add_executable(tests src/top.cpp)
verilate(tests
  PREFIX Vtop
  SOURCES src/top.sv
  TRACE
  PUBLIC)
