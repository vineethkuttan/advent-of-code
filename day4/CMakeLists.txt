cmake_minimum_required(VERSION 3.14)

# Day 1 executable
add_executable(day4
  day4.cpp
  day4.h)

# Confirm strictly to C++20
target_compile_features(day4 PUBLIC cxx_std_20)
set_target_properties(day4 PROPERTIES
  CXX_EXTENSIONS OFF
  CXX_STANDARD_REQUIRED ON)

# Link any required libraries to this console executable (currently none needed for hello world)
# target_link_libraries(day4 PRIVATE ...)

# Copy input.txt to build directory
configure_file(input.txt ${CMAKE_CURRENT_BINARY_DIR}/input.txt COPYONLY)