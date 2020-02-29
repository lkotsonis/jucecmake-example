cmake_minimum_required(VERSION 3.16)
project(jucecmake)

set (CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/third_party/juce-cmake/cmake; ${CMAKE_MODULE_PATH};")
set (JUCE_ROOT_DIR "${PROJECT_SOURCE_DIR}/third_party/JUCE/")

find_package(JUCE REQUIRED)
