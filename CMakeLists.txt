cmake_minimum_required(VERSION 3.13)
project(project-indigo)

set(CMAKE_CXX_STANDARD 14)
set(SFML_STATIC_LIBRARIES TRUE)
set(SFML_DIR "./sfml/lib/cmake/SFML")

find_package(SFML 2.5 COMPONENTS audio network graphics window system REQUIRED)
add_executable(project-indigo src/main.cpp)
target_link_libraries(project-indigo sfml-audio sfml-network sfml-graphics sfml-window sfml-system)