cmake_minimum_required(VERSION 3.10)

# Set project root (assuming the file is located in jni folder)
set(CMAKE_CURRENT_SOURCE_DIR ${CMAKE_SOURCE_DIR}/jni)

# Project name
project(serial_port)

# Target platform (NDK version can be specified here)
set(CMAKE_ANDROID_API_LEVEL 3)  # Adjust level as needed

# Source files
add_library(serial_port SHARED SerialPort.c)

# Link with system library (assuming logcat)
target_link_libraries(serial_port PUBLIC log)

# Shared library mode
set_target_properties(serial_port PROPERTIES POSITION_INDEPENDENT_CODE ON)
