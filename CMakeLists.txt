cmake_minimum_required(VERSION 3.31)
project(ymir-debugger)

set(CMAKE_CXX_STANDARD 20)

## Dependencies
include(FetchContent)
FetchContent_Declare(
    Catch2
    GIT_REPOSITORY https://github.com/catchorg/Catch2.git
    GIT_TAG        v3.15.0
)
FetchContent_MakeAvailable(Catch2)

add_subdirectory(vendor)

## Project targets
add_subdirectory(libs)
add_subdirectory(apps)
add_subdirectory(tests)
