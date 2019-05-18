cmake_minimum_required(VERSION 3.13)
project(project-indigo)

set(CMAKE_CXX_STANDARD 14)
set(SFML_DIR "C:/dev/libs/sfml/lib/cmake/SFML")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -IC:/dev/libs/sfml/include -LC:/dev/libs/sfml/lib")
set(SOURCE_FILES src/main.cpp)
set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake_modules)
find_package(SFML REQUIRED COMPONENTS audio network graphics window system)

include_directories(${SFML_INCLUDE_DIR})
add_executable(project-indigo src/main.cpp)
target_link_libraries(project-indigo sfml-audio sfml-network sfml-graphics sfml-window sfml-system)