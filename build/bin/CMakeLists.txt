add_executable(moReader ../../src/moFileReader/mo.cpp)

if( NOT COMPILE_DLL )
  add_definitions(-D_CONSOLE)
else()
  add_definitions(-D_CONSOLE -DMOFILE_IMPORT)
endif()

add_dependencies(moReader moFileReader)
target_link_libraries(moReader moFileReader)


