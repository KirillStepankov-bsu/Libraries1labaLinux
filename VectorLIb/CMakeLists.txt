cmake_minimum_required(VERSION 3.23)
project(VectorLIb)

set(CMAKE_CXX_STANDARD 17)

add_library(VectorLIb SHARED Vector.cpp)

add_library(NumbersLib STATIC IMPORTED)
set_target_properties(NumbersLib PROPERTIES INTERFACE_INCLUDE_DIRECTORIES ${CMAKE_CURRENT_SOURCE_DIR}/../NumbersLib)
set_target_properties(NumbersLib PROPERTIES IMPORTED_LOCATION ${CMAKE_CURRENT_SOURCE_DIR}/../NumbersLib/cmake-build-debug/libNumbersLib.a)
target_link_libraries(VectorLIb NumbersLib)