cmake_minimum_required(VERSION 3.12 FATAL_ERROR)
project(inchi LANGUAGES C VERSION 1.0.5)

add_compile_options("-Wall")

include_directories(/usr/local/include)

add_subdirectory(INCHI_BASE)
add_subdirectory(INCHI_API)
add_subdirectory(INCHI_DEMOS)
add_subdirectory(INCHI_EXE)
