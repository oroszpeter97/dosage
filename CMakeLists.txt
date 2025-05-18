cmake_minimum_required(VERSION 3.31)

project(dosage)

# Find OpenGL package
find_package(OpenGL REQUIRED)

# GLFW
find_package(glfw3 REQUIRED)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# Include directories
include_directories(include)
include_directories(include/core)

# Add executable
add_executable(dosage src/main.cpp src/core/Engine.cpp src/glad.c)

# Link GLFW, OpenGL
target_link_libraries(dosage glfw OpenGL::GL)