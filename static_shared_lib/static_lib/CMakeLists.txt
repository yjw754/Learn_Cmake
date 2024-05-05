cmake_minimum_required(VERSION 3.29.0)

project(my_static_lib LANGUAGES CXX)

#搜索所有的 cpp 文件
aux_source_directory(src SOURCES)

# 添加静态库并指定源文件
add_library(my_static_lib STATIC ${SOURCES})

target_include_directories(my_static_lib PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/inc")

