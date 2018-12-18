cmake_minimum_required(VERSION 2.8.9)
project(tinytiff)
set(CMAKE_BUILD_TYPE Release)
 
# bring the headers to the project
include_directories(".")

# and the source files
file(GLOB SOURCES "*.cpp")
 
# generate the shared library from the sources
add_library(tinytiff SHARED ${SOURCES})
 
# set the location for library installation
install(TARGETS tinytiff DESTINATION /usr/lib)
