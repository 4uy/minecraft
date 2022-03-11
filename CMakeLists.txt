cmake_minimum_required(VERSION 3.20)

# Set project name
project(minecraft)

# Set the C++ standard
set(CMAKE_CXX_STANDARD 17)

# Glob source files and compile them
file(GLOB_RECURSE SOURCES RELATIVE ${CMAKE_SOURCE_DIR} "src/*.cc" "src/*/*.cc")
add_executable(${PROJECT_NAME} ${SOURCES})
