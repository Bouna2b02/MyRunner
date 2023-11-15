cmake_minimum_required(VERSION 3.0)
project(MyRunner)

set(CMAKE_CXX_STANDARD 11)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

find_package(OpenGL REQUIRED)
find_package(glfw3 3.3 REQUIRED)

add_definitions(-DGL_SILENCE_DEPRECATION)

add_executable(my_runner src/main.cpp)

target_link_libraries(my_runner glfw ${OPENGL_LIBRARIES})
