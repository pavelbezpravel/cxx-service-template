cmake_minimum_required(VERSION 3.22)
project(awesome-service LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

add_executable(${PROJECT_NAME} main.cpp)
target_compile_options(${PROJECT_NAME}
    PRIVATE
        ${CXX_SERVICE_TEMPLATE_COMPILER_FLAGS}
)
target_link_libraries(${PROJECT_NAME}
    PRIVATE
        fmt::fmt
)
