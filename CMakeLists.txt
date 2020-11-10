cmake_minimum_required(VERSION 3.17)

project(cpp_example_project VERSION 1.0.0)

add_library(project_options INTERFACE)
target_compile_features(project_options INTERFACE cxx_std_14)

option(ENABLE_COVERAGE "Enable coverage reporting for  gcc/clang" FALSE)

if(ENABLE_COVERAGE)
    add_compile_options(--coverage -O0)
endif()

#include(cmake/Doxygen.cmake)
#enable_doxygen()

option(ENABLE_TESTING "Enable Test Builds" ON)

add_subdirectory(./src)

# include test dir
if(ENABLE_TESTING)
    enable_testing()
    add_subdirectory(./tests)
endif()