cmake_minimum_required(VERSION 3.6)
project(metamod CXX)

if (WIN32)
	message(FATAL_ERROR "CMakeLists.txt Windows platform isn't supported yet. Use msvc/metamod.sln instead it!")
endif()

add_custom_target(appversion DEPENDS
	COMMAND "${PROJECT_SOURCE_DIR}/metamod/version/appversion.sh" "${PROJECT_SOURCE_DIR}"
)

add_subdirectory(metamod)
