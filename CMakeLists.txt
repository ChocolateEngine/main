cmake_minimum_required( VERSION 3.18 FATAL_ERROR )

# use folders for visual studio
set_property( GLOBAL PROPERTY USE_FOLDERS ON )

set(CMAKE_CONFIGURATION_TYPES "Debug;Release;RelWithDebInfo;Profile")

# cringe for msvc runtime below
# https://cmake.org/cmake/help/latest/prop_tgt/MSVC_RUNTIME_LIBRARY.html
cmake_policy( SET CMP0091 NEW )

# Use these runtime libraries for both so it doesn't crash smh my head
# actually this is useless right now because of core.dll, god dammit
set_property( GLOBAL PROPERTY MSVC_RUNTIME_LIBRARY "MultiThreadedDLL" )

project( Sidury )

# Add Chocolate Framework DLLs
# add_subdirectory( ${CMAKE_CURRENT_LIST_DIR}/chocolate ${CMAKE_CURRENT_LIST_DIR}/chocolate )

message("value ${CMAKE_VS_WINDOWS_TARGET_PLATFORM_VERSION}")

# add_subdirectory( riff )
add_subdirectory( sidury )

message("value ${CMAKE_VS_WINDOWS_TARGET_PLATFORM_VERSION}")
