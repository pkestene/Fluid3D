cmake_minimum_required (VERSION 3.1)

project(Fluid3D CXX C)

# 
#set(CMAKE_CXX_STANDARD 11)
#set(CMAKE_CXX_EXTENSIONS OFF)


set(EXE_NAME Fluid3D)
add_executable(${EXE_NAME}
  array1.h
  array2.h
  array2_utils.h
  array3.h
  array3_utils.h
  fluidsim.h
  levelset_util.h
  util.h
  vec.h
  fluidsim.cpp
  levelset_util.cpp
  main.cpp)
target_include_directories(${EXE_NAME}
  PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}
  )

add_subdirectory(viewpls3D)
