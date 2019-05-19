cmake_minimum_required(VERSION 3.13)
project(project-indigo)

set(CMAKE_CXX_STANDARD 14)
set(SFML_STATIC_LIBARIES TRUE)
set(SFML_DIR "./sfml/lib/cmake/SFML")
set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -I./sfml/include -L./sfml/lib")
set(SOURCE_FILES src/main.cpp)
set(CMAKE_MODULE_PATH ${CMAKE_CURRENT_SOURCE_DIR}/cmake_modules)
find_package(SFML REQUIRED COMPONENTS audio network graphics window system)

include_directories(${SFML_INCLUDE_DIR})
add_executable(project-indigo src/main.cpp)
target_link_libraries(project-indigo sfml-audio sfml-network sfml-graphics sfml-window sfml-system)
file(COPY sfml/bin/sfml-audio-2.dll sfml/bin/sfml-graphics-2.dll sfml/bin/sfml-network-2.dll sfml/bin/sfml-system-2.dll sfml/bin/sfml-window-2.dll 
sfml/bin/sfml-audio-d-2.dll sfml/bin/sfml-graphics-d-2.dll sfml/bin/sfml-network-d-2.dll sfml/bin/sfml-system-d-2.dll sfml/bin/sfml-window-d-2.dll 
sfml/bin/openal32.dll DESTINATION /)