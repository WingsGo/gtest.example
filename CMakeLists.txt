cmake_minimum_required(VERSION 3.12)
project(gtest_example)

set(CMAKE_CXX_STANDARD 14)

# 添加头文件路径
include_directories(./include)

# 添加链接库路径
link_directories(./lib)
set(LIBRARIES
        gtest
        gtest_main
        pthread)

add_executable(gtest_example main.cpp)
target_link_libraries(gtest_example ${LIBRARIES})