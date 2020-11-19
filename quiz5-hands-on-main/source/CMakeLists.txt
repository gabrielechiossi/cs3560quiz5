cmake_minimum_required (VERSION 2.8.11)
project (Quiz5HandsOn)

set(CMAKE_BUILD_TYPE Debug)

add_library (Checker checkers.cc)
add_library (Game game.cc)
add_library (Space space.cc)

add_executable (checkers main.cc)

target_link_libraries (checkers LINK_PRIVATE Checker Game Space)
