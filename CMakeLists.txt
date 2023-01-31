cmake_minimum_required(VERSION 3.5)

project(asio VERSION 1.24.0)

add_library(asio INTERFACE)
set_target_properties(asio PROPERTIES INTERFACE_INCLUDE_DIRECTORIES ${ASIO_SRC_DIR})
