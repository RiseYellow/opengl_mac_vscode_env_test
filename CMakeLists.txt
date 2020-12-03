project(opengl_test)
cmake_minimum_required(VERSION 3.0)

include_directories(/usr/local/include)

aux_source_directory(src SRC) 

link_directories(/usr/local/lib)

add_executable(opengl_test ${SRC})

target_link_libraries(opengl_test glfw3 GLEW
"-framework OpenGL" 
"-framework Cocoa" 
"-framework GLUT"
"-framework IOKit"
"-framework CoreVideo")