cmake_minimum_required(VERSION 3.5)

project(scalapackfx VERSION 0.1 LANGUAGES Fortran)

set(SCALAPACK_LIBRARIES "scalapack" CACHE STRING "ScaLAPACK libraries")

set(INSTALL_BIN_DIR "bin")
set(INSTALL_MOD_DIR "include")
set(INSTALL_LIB_DIR "lib")

find_package(MPI REQUIRED)
include_directories(SYSTEM ${MPI_Fortran_INCLUDE_PATH})

add_subdirectory(src)
add_subdirectory(test)