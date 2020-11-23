cmake_minimum_required(VERSION 3.17)
project(piraten-kapern-client)

set(CMAKE_CXX_STANDARD 11)

set(CXX_FLAGS
        -Wall
        -std=c++11
        -lpthread
        )

link_libraries(pthread)

include_directories(
        include
)

set(CMAKE_BUILD_TYPE Debug)

set(CMAKE_CXX_COMPILER "g++")

set(SOURCE_FILES
    src/main.cpp
    src/client.cpp)

add_executable(pkclient  ${SOURCE_FILES})