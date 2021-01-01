cmake_minimum_required(VERSION 3.13)

project(fmgen LANGUAGES CXX)

add_library(fmgen
  fmgen/fmtimer.cpp
  fmgen/opna.cpp
  fmgen/fmgen.cpp
  fmgen/opm.cpp
  fmgen/psg.cpp)

target_include_directories(fmgen PUBLIC .)

if (MSVC)
  target_compile_definitions(fmgen PRIVATE _CRT_SECURE_NO_WARNINGS)
  target_compile_options(fmgen PRIVATE /utf-8)
endif()
