cmake_minimum_required(VERSION 3.10)
project(test-opengl)

set(CMAKE_CXX_STANDARD 11)

find_package(glfw3 3.3 REQUIRED)
find_package(OpenGL REQUIRED)

include_directories(${CMAKE_SOURCE_DIR}/include)
include_directories(${CMAKE_SOURCE_DIR}/src/glad/include)

add_executable(test-opengl main.cpp src/glad/glad.c)

target_link_libraries(test-opengl glfw OpenGL::GL)