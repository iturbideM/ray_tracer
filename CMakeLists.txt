cmake_minimum_required(VERSION 3.10.0)
project(ray_tracer VERSION 0.1.0 LANGUAGES C CXX)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

# Disable CRT secure warnings on Windows
add_compile_definitions(_CRT_SECURE_NO_WARNINGS)

# Add include directories
include_directories(
    ${CMAKE_SOURCE_DIR}/include/core
    ${CMAKE_SOURCE_DIR}/include/geometry
    ${CMAKE_SOURCE_DIR}/include/materials
    ${CMAKE_SOURCE_DIR}/include/external
    ${CMAKE_SOURCE_DIR}/external
)

add_executable(ray_tracer src/main.cpp)

