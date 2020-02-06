#
# project: sokol
#

if (NOT FIPS_IMPORT)
    message("NOT IMPORT")
    cmake_minimum_required(VERSION 2.8)
    get_filename_component(FIPS_ROOT_DIR "../fips" ABSOLUTE)
    include("${FIPS_ROOT_DIR}/cmake/fips.cmake")
    fips_setup()
    project(fips-sokol)
    fips_project(fips-sokol)
endif()
# select the 3D backend for sokol_gfx.h and sokol_app.h
# the sokol_config() macro is in the top-level CMakeLists.txt file!
sokol_config()


fips_include_directories(sokol sokol/util)
fips_add_subdirectory(entry)

if (NOT FIPS_IMPORT)
    fips_finish()
endif()