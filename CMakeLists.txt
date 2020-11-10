cmake_minimum_required(VERSION 3.17)

project(cpp_example_project VERSION 1.0.0)

add_library(project_options INTERFACE)
target_compile_features(project_options INTERFACE cxx_std_17)

#set(CMAKE_CXX_STANDARD 14)
#set(CMAKE_CXX_STANDARD_REQUIRED ON)
#set(CMAKE_CXX_EXTENSIONS OFF)

add_subdirectory(./src)