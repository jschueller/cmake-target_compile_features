cmake_minimum_required (VERSION 3.0)

set(CMAKE_BUILD_TYPE "Release" CACHE STRING "Choose the build type")

project (hello)

add_executable (hello main.cxx)
target_compile_features(hello
         PUBLIC
            cxx_lambdas
            cxx_auto_type)

install (TARGETS hello DESTINATION bin)
