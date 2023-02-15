cmake_minimum_required(VERSION 3.5)

project(asio VERSION 1.24.0)

add_library(asio INTERFACE)
target_include_directories(asio PUBLIC INTERFACE  "${PROJECT_SOURCE_DIR}/asio-v1.24.0")

if(${CMAKE_CURRENT_SOURCE_DIR} STREQUAL ${CMAKE_SOURCE_DIR})
    add_subdirectory(test)
endif()
