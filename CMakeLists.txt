cmake_minimum_required(VERSION 3.31)

project("mobius-chess")

find_package(GLEW CONFIG REQUIRED)
find_package(glfw3 CONFIG REQUIRED)
find_package(glm CONFIG REQUIRED)

add_executable(mobiuschess
    mobiuschess.cpp
    mobiuschess.h
)

target_compile_features(mobiuschess PRIVATE cxx_std_20)

target_link_libraries(mobiuschess PRIVATE
    GLEW::GLEW
    glfw
    glm::glm
)