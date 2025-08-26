cmake_minimum_required(VERSION 3.10)
project(c_project)

# 收集 src 下的所有 .c
file(GLOB SRC_FILES CONFIGURE_DEPENDS
     "${CMAKE_SOURCE_DIR}/src/*.c")

add_executable(main ${SRC_FILES})

# 让编译器能找到 inc 里的头文件
target_include_directories(main PRIVATE
    "${CMAKE_SOURCE_DIR}/include"
)
