find_package(OpenGL REQUIRED)
find_package(GLUT REQUIRED)

include_directories(${OPENGL_INCLUDE_DIR} ${GLUT_INCLUDE_DIRS})

set(EXE_NAME viewpls3D)

add_executable(${EXE_NAME}
  gluvi.cpp
  gluvi.h
  util.h
  vec.h
  main.cpp)
target_include_directories(${EXE_NAME}
  PUBLIC
  ${CMAKE_CURRENT_SOURCE_DIR}
  )
target_link_libraries(${EXE_NAME} ${OPENGL_LIBRARIES} ${GLUT_LIBRARY})
