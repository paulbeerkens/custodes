cmake_minimum_required(VERSION 3.8)

project(Custodes VERSION 1.0.0 LANGUAGES CXX)

set(CMAKE_CXX_STANDARD 17)

include(cmake/StandardProjectSettings.cmake)
#add_compile_options(-Wall -Wextra -pedantic -Werror)


# Link this 'library' to use the warnings specified in CompilerWarnings.cmake
add_library(project_warnings INTERFACE)
include(cmake/CompilerWarnings.cmake)
set_project_warnings(project_warnings)

add_subdirectory(src)
add_subdirectory(external)