cmake_minimum_required(VERSION 3.29.0)

project(my_shared_lib LANGUAGES CXX)

aux_source_directory(src SOURCES)

add_library(my_shared_lib SHARED ${SOURCES})

target_include_directories(my_shared_lib PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/inc")

