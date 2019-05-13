

cmake_minimum_required (VERSION 2.8.12)

set(CMAKE_BUILD_TYPE "Release" CACHE STRING "Choose the build type")

if(POLICY CMP0025)
  cmake_policy(SET CMP0025 NEW)
endif()

project (hello)



add_executable (hello main.cxx)

if (NOT CMAKE_VERSION VERSION_LESS 3.1)
  target_compile_features (hello PUBLIC cxx_lambdas cxx_auto_type)
endif ()

install (TARGETS hello DESTINATION bin)
