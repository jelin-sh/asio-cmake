cmake_minimum_required(VERSION 3.5)

project(asio VERSION 1.24.0)

add_library(asio INTERFACE)
#set_target_properties(asio PROPERTIES  ${ASIO_SRC_DIR})
target_include_directories(asio PUBLIC INTERFACE  "${PROJECT_SOURCE_DIR}/asio-v1.24.0")

if(1)
    add_subdirectory(test)
endif()
