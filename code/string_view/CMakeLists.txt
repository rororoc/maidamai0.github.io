cmake_minimum_required(VERSION 3.10)

get_filename_component(TARGET ${CMAKE_CURRENT_SOURCE_DIR} NAME)
project(${TARGET} CXX)

find_package(fmt CONFIG REQUIRED)
link_libraries(fmt::fmt-header-only)

file(GLOB src "*.cpp")

add_executable(${TARGET} ${src})