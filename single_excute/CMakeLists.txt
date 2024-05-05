#指定需要的CMake最低版本
cmake_minimum_required(VERSION 3.29.0)

# 设置 C++ 标准
set(CMAKE_CXX_STANDARD 14)
set(CMAKE_CXX_STANDARD_REQUIRED True)

#定义项目名称、版本号、支持的语言
project(SINGLE_EXCUTE VERSION 0.1.0 LANGUAGES CXX)

#添加一个可执行文件"SINGLE_EXCUTE"，该文件的源代码是"main.cpp"
add_executable(SINGLE_EXCUTE main.cpp)

# 添加头文件目录,以便引用该头文件
target_include_directories(SINGLE_EXCUTE PUBLIC "${CMAKE_CURRENT_SOURCE_DIR}/print/inc")

# 向目标文件添加源文件，使得 CMake 在构建项目时会将这个源文件一起编译进主项目
target_sources(SINGLE_EXCUTE PRIVATE
    "${CMAKE_CURRENT_SOURCE_DIR}/print/src/print.cpp"
)