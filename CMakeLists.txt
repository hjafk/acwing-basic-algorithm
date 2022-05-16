cmake_minimum_required(VERSION 3.22)
project(acwing_basic_algorithm)

set(CMAKE_CXX_STANDARD 17)

file (GLOB_RECURSE files *.cpp)
foreach (file ${files})
    string(REGEX REPLACE ".+/(.+)/(.+)\\..*" "\\1-\\2" exe ${file})
    add_executable (${exe} ${file})
endforeach ()
