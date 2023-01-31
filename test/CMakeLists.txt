cmake_minimum_required(VERSION 3.5)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_EXTENSIONS OFF)

project(
    asio_test
    VERSION 1.0.0
    LANGUAGES C CXX
)

find_package(Threads REQUIRED)

add_executable(asio_test main.cpp)
target_link_libraries(asio_test asio ws2_32 wsock32)
target_compile_definitions(asio_test PRIVATE _WIN32_WINNT=0x0A00 ASIO_STANDALONE)