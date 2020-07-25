file(GLOB inchi_sources src/*.c)
add_compile_definitions(TARGET_API_LIB=1, COMPILE_ANSI_ONLY=1)
add_library(inchi STATIC ${inchi_sources})
target_include_directories(inchi PUBLIC include)
install(TARGETS inchi DESTINATION lib)
install(
    DIRECTORY include
    DESTINATION include
    FILES_MATCHING PATTERN "*.h"
)
