set(CMAKE_BUILD_TYPE "Debug")

#claim a cmake_version
cmake_minimum_required(VERSION 2.8)

#claim a cmake project
project(HelloSLAM)

#add an exe
#add_executable(program_name soure)
add_executable(helloSLAM helloSLAM.cpp)
add_library(hello_shared SHARED libHelloSLAM.cpp)

add_executable(useHello useHello.cpp)
target_link_libraries(useHello hello_shared)
