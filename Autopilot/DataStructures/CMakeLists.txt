# CMakeLists for DataStructures library
cmake_minimum_required(VERSION 3.2.0)
project(DataStructures CXX)

file(GLOB_RECURSE DATASTRUCTURES_SOURCES "${CMAKE_CURRENT_SOURCE_DIR}/Src/*.cpp")
file(GLOB_RECURSE DATASTRUCTURES_HEADERS "${CMAKE_CURRENT_SOURCE_DIR}/Inc/*.hpp")

add_library(${PROJECT_NAME} STATIC ${DATASTRUCTURES_SOURCES} ${DATASTRUCTURES_HEADERS})

target_include_directories(${PROJECT_NAME} PUBLIC
    ${CMAKE_CURRENT_SOURCE_DIR}/Src
    ${CMAKE_CURRENT_SOURCE_DIR}/Inc
)
