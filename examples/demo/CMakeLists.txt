if (CMAKE_CURRENT_SOURCE_DIR STREQUAL CMAKE_SOURCE_DIR)
    cmake_minimum_required(VERSION 3.14...3.28)
    project(ggml-demo C CXX)
    set(CMAKE_RUNTIME_OUTPUT_DIRECTORY "${CMAKE_BINARY_DIR}/bin")
    add_subdirectory("../.." "${CMAKE_BINARY_DIR}/ggml")
endif()

add_executable(demo demo.c)
target_link_libraries(demo PRIVATE ggml)
