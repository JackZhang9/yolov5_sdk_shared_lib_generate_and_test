cmake_minimum_required(VERSION 3.1)

set(PROJECT_NAME "demo")

set(EXECUTABLE_OUTPUT_PATH ${PROJECT_SOURCE_DIR})
find_package(OpenCV REQUIRED)
include_directories(${PROJECT_SOURCE_DIR}/include)

link_directories(${PROJECT_SOURCE_DIR}/lib)

add_executable(${PROJECT_NAME} main.cpp)

target_link_libraries(${PROJECT_NAME} ${OpenCV_LIBS} detectJS)
