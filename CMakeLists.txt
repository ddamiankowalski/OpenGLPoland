cmake_minimum_required(VERSION 3.0.0)
project(opengl_practice VERSION 0.1.0)
cmake_policy(SET CMP0072 NEW)

find_package(OpenGL REQUIRED)

add_executable(
    opengl_practice 
    src/main.cpp
    src/glad.c 
    src/glad.h
    src/shader.h
    src/camera.h
    src/geodata.h
    src/vertexarray.h
    src/stb_image.h
)

target_link_libraries(opengl_practice glfw)

target_link_libraries(
    opengl_practice
    glfw
    OpenGL::GL
)