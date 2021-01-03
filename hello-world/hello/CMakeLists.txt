add_library(hello STATIC hello.c)

# `target_xxx` command series have a common effect: property propagation through
# target. Let's talk more w.r.t. this command:
# 1) INTERFACE: propagate this include directory through target 'library hello'
#   to anyone who use this library;
# 2) PRIVATE: do not propagate through libhello ,(and thanks to this, nobody
#   could see this include directory anymore) but only avalible for source file
#   hello.c;
# 3) PUBLIC: a combination of INTERFACE and PRIVATE
target_include_directories(hello INTERFACE "${CMAKE_CURRENT_SOURCE_DIR}")