cmake_minimum_required(VERSION 2.8)
project(sjasm)
file(GLOB sjasm_SRC
    "src/*.h"
    "src/*.cpp"
)
add_executable(sjasm ${sjasm_SRC})
install_targets(/bin sjasm)
