add_library(world STATIC world.c)
target_include_directories(world INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}")