cmake_minimum_required(VERSION 2.8.10)
set(CMAKE_MODULE_PATH ${CMAKE_SOURCE_DIR}/cmake ${CMAKE_SOURCE_DIR}/cmake/deps)
project(font-render C)
set(PROJECT_VERSION 0.0.1)

set(EXTRA_FLAGS "-Wall -pedantic")
set(CMAKE_C_FLAGS "${CMAKE_C_FLAGS} ${EXTRA_FLAGS}")
set(CMAKE_C_FLAGS_RELEASE "${CMAKE_C_FLAGS_RELEASE} -O2 -DNDEBUG")
set(CMAKE_C_FLAGS_DEBUG "${CMAKE_C_FLAGS_DEBUG} -O0")

set(BINARY_OUTPUT_DIR ${CMAKE_BINARY_DIR}/bin)
set(LIB_OUTPUT_DIR ${CMAKE_BINARY_DIR}/lib)
set(INCLUDE_OUTPUT_DIR ${CMAKE_BINARY_DIR}/include)

file(MAKE_DIRECTORY ${BINARY_OUTPUT_DIR})
file(MAKE_DIRECTORY ${LIB_OUTPUT_DIR})
file(MAKE_DIRECTORY ${INCLUDE_OUTPUT_DIR})

set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${BINARY_OUTPUT_DIR})
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${LIB_OUTPUT_DIR})

add_subdirectory(src)
