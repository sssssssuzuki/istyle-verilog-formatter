cmake_minimum_required(VERSION 3.10)

project(istyle-verilog-formatter)

set (CMAKE_CXX_STANDARD 17)

file(GLOB cpp_files src/astyle/*.cpp)
file(GLOB h_files src/*.h)
add_executable(istyle src/astyle_main.cpp ${cpp_files} ${h_files})
include_directories(src)
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} /wd4068 /wd4819 /D _SILENCE_CXX17_RESULT_OF_DEPRECATION_WARNING")
