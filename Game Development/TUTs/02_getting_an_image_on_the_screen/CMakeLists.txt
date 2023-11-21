cmake_minimum_required(VERSION 3.10)

project(test)

set( FILES
    02_getting_an_image_on_the_screen.cpp
)

find_package(SDL2 REQUIRED)

include_directories(
    include
    ${SDL2_INCLUDE_DIRS}
)

add_executable(${PROJECT_NAME} ${FILES})

target_link_libraries(test ${SDL2_LIBRARIES})