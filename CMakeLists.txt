cmake_minimum_required(VERSION 3.5)
project(sjasm)
set(CMAKE_CXX_STANDARD 11)
file(GLOB sjasm_SRC
    "src/*.h"
    "src/*.cpp"
)
add_executable(sjasm ${sjasm_SRC})
if(CMAKE_COMPILER_IS_GNUCXX)
    set(CMAKE_CXX_FLAGS "-Wno-switch-bool")
endif()
install_targets(/bin sjasm)
