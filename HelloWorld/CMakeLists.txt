cmake_minimum_required(VERSION 3.0.0)
project(HelloWorld VERSION 0.1.0)

include_directories(./include)
link_directories(./lib)

include(CTest)
enable_testing()

add_executable(HelloWorld ./src/main.c)
target_link_libraries(HelloWorld )

set(CPACK_PROJECT_NAME ${PROJECT_NAME})
set(CPACK_PROJECT_VERSION ${PROJECT_VERSION})
set(CMAKE_VERBOSE_MAKEFILE true)

include(CPack)
