cmake_minimum_required(VERSION 3.10)

project(OpenGLScene)

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(OpenGLScene main.cpp)

add_subdirectory(external/glfw)
target_link_libraries(OpenGLScene PRIVATE glfw)

target_include_directories(OpenGLScene PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/external/glad/include
)
target_sources(OpenGLScene PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/external/glad/src/glad.c
)