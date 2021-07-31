cmake_minimum_required(VERSION 3.20)

project(imgui-template C CXX)

include(${CMAKE_BINARY_DIR}/conanbuildinfo.cmake)
conan_basic_setup()

set(CMAKE_CXX_STANDARD 17)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_subdirectory(dependency)


add_executable(imgui-template main.cpp)
# target_include_directories(imgui-template )
target_link_libraries(imgui-template ${CONAN_LIBS})
target_link_libraries(imgui-template imgui implot)

# add_subdirectory(examples)