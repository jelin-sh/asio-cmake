cmake_minimum_required(VERSION 3.5)

project(asio_test VERSION 1.0.0)

find_package(Threads REQUIRED)

add_executable(asio_test main.cpp)
target_link_libraries(asio_test asio)
target_compile_definitions(asio_test PRIVATE _WIN32_WINDOWS )