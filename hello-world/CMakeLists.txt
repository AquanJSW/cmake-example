add_library(hello-world STATIC hello_world.c)

# The following 2 commands is ready for `target_link_libraries`, cause the
# latter command needs libraries named 'hello' and 'world', which could be 
# satisfied by using this 2 commands. (`add_subdirectory` gives cmake the
# permission to find necessary dependencies under this directories while 
# building)
add_subdirectory(hello)
add_subdirectory(world)
target_link_libraries(hello-world PRIVATE hello world)
target_include_directories(hello-world INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}")