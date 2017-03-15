project(hello-world)
cmake_minimum_required(VERSION 3.2)

enable_testing()

set(MORPHOTOOL_VERSION_MAJOR "1")
set(MORPHOTOOL_VERSION_MINOR "2")

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR}/CMake
      ${PROJECT_SOURCE_DIR}/CMake/portability
      ${PROJECT_SOURCE_DIR}/CMake/packages
      ${PROJECT_SOURCE_DIR}/CMake/config)

include(DefineInstallationPaths)
include(ReleaseDebugAutoFlags)
include(BlueGenePortability)

find_package(MPI)

include(BlueGenePortability)

add_subdirectory(src)


