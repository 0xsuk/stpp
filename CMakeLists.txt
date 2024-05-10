cmake_minimum_required(VERSION 3.1)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_EXPORT_COMPILE_COMMANDS on)

project(stpp)

find_package(Freetype REQUIRED)
find_package(X11 REQUIRED)

include_directories(${FREETYPE_INCLUDE_DIRS})

add_executable(${PROJECT_NAME}
  x.cpp
  )
target_link_libraries(${PROJECT_NAME} freetype X11 util Xft m rt)
