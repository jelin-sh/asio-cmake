cmake_minimum_required(VERSION 3.5)

project(asio VERSION 1.24.0)

find_package(Threads REQUIRED)
add_library(asio INTERFACE)
target_include_directories(asio PUBLIC INTERFACE "${PROJECT_SOURCE_DIR}/asio-v1.24.0")
if (${CMAKE_SYSTEM_NAME} STREQUAL "Windows")
    target_link_libraries(asio INTERFACE ws2_32 wsock32)
    target_compile_definitions(asio INTERFACE _WIN32_WINNT=0x0A00 ASIO_STANDALONE)
endif ()

if (${CMAKE_CURRENT_SOURCE_DIR} STREQUAL ${CMAKE_SOURCE_DIR})
    add_subdirectory(test)
endif ()
