cmake_minimum_required(VERSION 3.5)
project(GravitySim)
set (CMAKE_CXX_STANDARD 14)

#LINKING SHARED LIBRARIES
set( PROJECT_LINK_LIBS libGL.so.1)

#glfw library
set( GLFW_LINK_LIBS libglfw.so )

#set( GDAL_LINK_LIBS libgdal.so )

link_directories(/snap/gnome-3-26-1604/74/usr/lib/x86_64-linux-gnu/mesa/ /usr/local/lib/)

#ADDING INCLUDE DIRECTORIES
include_directories(/usr/local/include/ include )

file(GLOB SOURCES "src/*")

add_executable(gravitysim ${SOURCES})

target_link_libraries(gravitysim ${PROJECT_LINK_LIBS} ${GLFW_LINK_LIBS} ${CMAKE_DL_LIBS})
