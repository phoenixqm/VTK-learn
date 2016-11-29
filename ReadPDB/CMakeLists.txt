
cmake_minimum_required(VERSION 2.8)

PROJECT(ReadPDB)

find_package(VTK REQUIRED)
include(${VTK_USE_FILE})

add_executable(ReadPDB MACOSX_BUNDLE ReadPDB)

if(VTK_LIBRARIES)
  target_link_libraries(ReadPDB ${VTK_LIBRARIES})
else()
  target_link_libraries(ReadPDB vtkHybrid vtkWidgets)
endif()
