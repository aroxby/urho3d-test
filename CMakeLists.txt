cmake_minimum_required(VERSION 2.6)

set(PROJECT_NAME urho3d-test)
project(${PROJECT_NAME})

set(CMAKE_MODULE_PATH ${CMAKE_MODULE_PATH} ${CMAKE_SOURCE_DIR}/cmake)
find_package(Urho3D REQUIRED)

file(GLOB SRCS *.cpp)

include_directories(${URHO3D_INCLUDE_DIRS})

add_executable(${PROJECT_NAME} ${SRCS})

target_link_libraries(${PROJECT_NAME} ${URHO3D_LIBRARIES})
