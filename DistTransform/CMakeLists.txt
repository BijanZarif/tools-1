cmake_minimum_required(VERSION 2.8)

PROJECT(DistanceTransformMesh)

FIND_PACKAGE(VTK 7 REQUIRED)

FIND_PACKAGE(Armadillo REQUIRED)
include_directories(${ARMADILLO_INCLUDES})

INCLUDE(${VTK_USE_FILE})

#needed for the unordered_map
SET(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11") 

ADD_EXECUTABLE(DistanceTransformMesh DistanceTransformMesh.cpp)
TARGET_LINK_LIBRARIES(DistanceTransformMesh  ${VTK_LIBRARIES} ${ARMADILLO_LIBRARIES})


