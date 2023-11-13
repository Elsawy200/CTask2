cmake_minimum_required(VERSION 3.26)
project(Project C)

set(CMAKE_C_STANDARD 11)

# Add MPI Package to Project
find_package(MPI REQUIRED)

# Add your source files
add_executable(Project main.c)

# Link MPI libraries
target_link_libraries(Project PRIVATE MPI::MPI_C)