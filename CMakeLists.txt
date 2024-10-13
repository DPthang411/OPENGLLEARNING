cmake_minimum_required(VERSION 3.30.3)
project(OPENGL)
add_library(glfw SHARED IMPORTED)
target_include_directories(glfw SYSTEM INTERFACE ${PROJECT_SOURCE_DIR}/third-party/GLFW/include)
set_target_properties(glfw PROPERTIES
    IMPORTED_LOCATION ${PROJECT_SOURCE_DIR}/third-party/GLFW/glfw3.dll)
add_executable(OPENGL main.cpp)
target_link_libraries(OPENGL PUBLIC glfw)