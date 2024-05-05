cmake_minimum_required(VERSION 3.29.0)

project(my_main LANGUAGES CXX)

add_executable(my_main main.cpp)

add_subdirectory(static_lib)
add_subdirectory(shared_lib)

target_link_libraries(my_main PRIVATE
 my_static_lib
 my_shared_lib
 )
