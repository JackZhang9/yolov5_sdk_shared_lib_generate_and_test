cmake_minimum_required(VERSION 3.1)

set(PROJECT_NAME "detectJS")

find_package(OpenCV REQUIRED)

add_library(${PROJECT_NAME} SHARED interface.h detectJZ.cpp)

target_link_libraries(${PROJECT_NAME} PRIVATE ${OpenCV_LIBS})
