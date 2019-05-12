cmake_minimum_required (VERSION 2.8)

if (NOT DEFINED CMAKE_BUILD_TYPE)
  set (CMAKE_BUILD_TYPE Release CACHE STRING "Build type")
endif ()

project (hello)

add_executable (hello main.cxx)
target_compile_features(hello
         PUBLIC 
            cxx_rvalue_references
            cxx_variadic_templates
            cxx_lambdas
            cxx_defaulted_move_initializers
            cxx_delegating_constructors
            cxx_thread_local
            cxx_constexpr
            cxx_decltype_incomplete_return_types
            cxx_auto_type)

install (TARGETS hello DESTINATION bin)
