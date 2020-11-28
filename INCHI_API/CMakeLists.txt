add_compile_definitions(TARGET_API_LIB=1, COMPILE_ANSI_ONLY=1)
file(GLOB inchi_api_sources src/*.c)
add_library(inchi_api STATIC ${inchi_api_sources})
target_include_directories(inchi_api PUBLIC include)
target_link_libraries(inchi_api inchi_base)

file(GLOB inchi_ixa_sources src/ixa/*.c)
add_library(inchi_ixa STATIC ${inchi_ixa_sources})
target_include_directories(inchi_ixa PUBLIC include/ixa)
target_link_libraries(inchi_ixa inchi_base inchi_api)

file(GLOB inchi_ixa_test_sources test/ixa/*.c)
add_executable(inchi_ixa_test ${inchi_ixa_test_sources})
target_link_libraries(inchi_ixa_test inchi_api inchi_base inchi_ixa)
