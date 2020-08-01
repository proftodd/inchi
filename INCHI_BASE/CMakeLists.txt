add_compile_definitions(TARGET_API_LIB=1, COMPILE_ANSI_ONLY=1)
file(GLOB inchi_base_sources src/*.c)
add_library(inchi_base STATIC ${inchi_base_sources})
target_include_directories(inchi_base PUBLIC include)
install(TARGETS inchi_base DESTINATION lib)
install(
    DIRECTORY include
    DESTINATION include
    FILES_MATCHING PATTERN "*.h"
)
