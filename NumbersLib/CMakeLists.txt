cmake_minimum_required(VERSION 3.23)
project(NumbersLib)

set(CMAKE_CXX_STANDARD 17)

add_compile_options(-fPIC)
add_library(NumbersLib STATIC number.cpp)
