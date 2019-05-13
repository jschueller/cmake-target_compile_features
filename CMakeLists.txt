
if (POLICY CMP0025)
 cmake_policy(SET CMP0025 NEW)
endif()

cmake_minimum_required (VERSION 2.8.12)

set(CMAKE_BUILD_TYPE "Release" CACHE STRING "Choose the build type")

project (hello)

add_executable (hello main.cxx)

if (NOT CMAKE_VERSION VERSION_LESS 3)
  target_compile_features (hello PUBLIC cxx_lambdas cxx_auto_type)
endif ()

install (TARGETS hello DESTINATION bin)
