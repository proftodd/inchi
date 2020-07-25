cmake_minimum_required(VERSION 3.0 FATAL_ERROR)
project(inchi LANGUAGES C VERSION 1.0.5)

add_compile_options("-Wall")

include_directories(/usr/local/include)

add_subdirectory(INCHI_BASE)
