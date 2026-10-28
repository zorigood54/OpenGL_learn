cmake_minimum_required(VERSION 3.10)
project(OpenGL_learn)
set(CMAKE_CXX_STANDARD 17)
find_package(glfw3 REQUIRED)
find_package(OpenGL REQUIRED)
include_directories(include)
add_executable(OpenGL_learn
    src/main.cpp
    src/glad.c
)
target_link_libraries(OpenGL_learn PRIVATE glfw OpenGL::GL)

file(COPY ${CMAKE_SOURCE_DIR}/shaders DESTINATION ${CMAKE_BINARY_DIR})