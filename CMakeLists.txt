cmake_minimum_required(VERSION 3.20)

# Set project name
project(minecraft)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)

# Glob source files and compile them
file(GLOB_RECURSE SOURCES RELATIVE ${CMAKE_SOURCE_DIR} "src/*.cc" "src/*/*.cc")
add_executable(${PROJECT_NAME} ${SOURCES})

# bgfx.cmake
add_subdirectory(lib/bgfx.cmake)
target_link_libraries(${PROJECT_NAME} bgfx bimg bx)

# GLFW
add_subdirectory(lib/glfw)
target_link_libraries(${PROJECT_NAME} glfw)
