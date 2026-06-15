cmake_minimum_required(VERSION 4.2) #initial cmake setup and version enforcement.
set(CMAKE_CXX_STANDARD 17) #/
message(STATUS "CMake Version: ${CMAKE_VERSION}") #/

set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Release>:Release>") #These lines come highly reccomended by LowLevelGameDev; 
set(CMAKE_MSVC_RUNTIME_LIBRARY "MultiThreaded$<$<CONFIG:Debug>:Debug>") #/


project(LabRat VERSION 0.01 DESCRIPTION "LabRat game engine")
 

add_subdirectory("engine") #Engine code


#Lib definition etc. is down a cmake level.


add_executable(LabRat)
target_sources(LabRat