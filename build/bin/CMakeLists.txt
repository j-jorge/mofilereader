add_executable(moReader ../../src/moFileReader/mo.cpp)

if ( NOT COMPILE_DLL )

add_definitions(-D_CONSOLE)
add_dependencies(moReader moFileReader.static)
target_link_libraries(moReader moFileReader.static)

else ( COMPILE_DLL )

add_definitions(-D_CONSOLE -DMOFILE_IMPORT)
add_dependencies(moReader moFileReader)
target_link_libraries(moReader moFileReader)

endif ()



