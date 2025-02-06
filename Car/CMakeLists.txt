cmake_minimum_required(VERSION 3.10)
project(CarProject)

set(CMAKE_CXX_STANDARD 17)

find_package(SFML 2.5 COMPONENTS graphics window system REQUIRED)

add_executable(CarProject src/main.cpp src/Car.cpp)
target_include_directories(CarProject PRIVATE ${SFML_INCLUDE_DIRS} include)
target_link_libraries(CarProject PRIVATE sfml-graphics sfml-window sfml-system)