cmake_minimum_required(VERSION 3.22)
project(CXX-SERVICE-TEMPLATE LANGUAGES CXX)

set(BUILD_SHARED_LIBS OFF)
set(CMAKE_CXX_STANDARD 20)
set(CMAKE_CXX_EXTENSIONS OFF)
set(CMAKE_CXX_STANDARD_REQUIRED ON)

# TODO [pavelbezpravel]: support Clang and MSVC.
if(CMAKE_CXX_COMPILER_ID MATCHES "GNU")
    include(cmake/flags.compiler.gnu.cmake)
endif()

add_subdirectory(src)
