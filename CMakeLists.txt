cmake_minimum_required(VERSION 3.16)
project(jucecmake)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set (CMAKE_MODULE_PATH "${PROJECT_SOURCE_DIR}/third_party/juce-cmake/cmake; ${CMAKE_MODULE_PATH};")
set (JUCE_ROOT_DIR "${PROJECT_SOURCE_DIR}/third_party/JUCE/")

if (NOT DEFINED CMAKE_BUILD_TYPE)
  set(CMAKE_BUILD_TYPE "Release")
endif()

find_package(JUCE REQUIRED
  COMPONENTS
  juce_audio_basics
  juce_audio_devices
  juce_core
  juce_events
  juce_gui_basics)

set(SOURCES src/Main.cpp)

add_executable(${PROJECT_NAME} ${SOURCES})
target_link_libraries(${PROJECT_NAME} ${JUCE_LIBRARIES})
