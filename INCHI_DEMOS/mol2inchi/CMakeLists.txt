add_executable(mol2inchi src/mol2inchi.c src/moreutil.c)
target_include_directories(mol2inchi PUBLIC include)
target_link_libraries(mol2inchi inchi_base inchi_api)
# TODO: How to require presence of OpenMP