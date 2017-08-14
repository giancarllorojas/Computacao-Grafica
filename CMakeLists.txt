cmake_minimum_required(VERSION 3.8)
project(compgraf)

set(CMAKE_C_STANDARD 11)

set(SOURCE_FILES main.c)
add_executable(compgraf ${SOURCE_FILES})

find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)
include_directories( ${OPENGL_INCLUDE_DIRS}  ${GLUT_INCLUDE_DIRS} )

target_link_libraries(compgraf ${OPENGL_LIBRARIES} ${GLUT_LIBRARY} )