cmake_minimum_required(VERSION 3.30)

project(hwid_poc)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_STANDARD_REQUIRED ON)
set(CMAKE_BUILD_PARALLEL_LEVEL 8 STRING)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR})

message("\n======== Hwid_poc ========")

if(${CMAKE_SOURCE_DIR} STREQUAL ${CMAKE_CURRENT_SOURCE_DIR})
    option(HWID_POC_BUILD_TESTS      "Build tests"      ON)
    option(HWID_POC_BUILD_BENCHMARKS "Build benchmarks" ON)
else()
    option(HWID_POC_BUILD_TESTS      "Build tests"      OFF)
    option(HWID_POC_BUILD_BENCHMARKS "Build benchmarks" OFF)
endif()

if(${HWID_POC_BUILD_TESTS})
    enable_testing()
endif()

add_subdirectory(cmake)
add_subdirectory(src)
