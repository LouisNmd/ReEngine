cmake_minimum_required(VERSION 3.5)
project(ReEngine VERSION 0.1.0 LANGUAGES C CXX)

include(C:/dev/vcpkg/scripts/buildsystems/vcpkg.cmake)

add_executable(main main.cpp)

find_package(GLEW REQUIRED)
target_link_libraries(main PRIVATE GLEW::GLEW)

find_package(glfw3 CONFIG REQUIRED)
target_link_libraries(main PRIVATE glfw)

find_package(OpenGL REQUIRED)
target_link_libraries(main PRIVATE OpenGL::GL)

include(CTest)
enable_testing()

