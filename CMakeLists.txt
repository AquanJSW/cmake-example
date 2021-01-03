cmake_minimum_required(VERSION 3.5)

project(cmake-hello-world)

set(C_STANDARD 99)
set(C_STANDARD_REQUIRED)

add_executable(cmake-hello-world main.c)

add_subdirectory(hello-world)

target_link_libraries(cmake-hello-world hello-world)