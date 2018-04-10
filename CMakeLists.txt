################################################################################
# Template CMake file for C/C++11 projects.
################################################################################

# Using functionality present in the 3.0.2 CMake documentation.
cmake_minimum_required (VERSION 3.0.2)

# project(<PROJECT-NAME>
#        [VERSION <major>[.<minor>[.<patch>[.<tweak>]]]]
#		 [LANGUAGES <language-name>...])
# The project's name is "Template".
# Set version is 1 Major and 0 Minor.
# This project uses C and CXX (CXX = C++) languages.
project(Template VERSION 1.0 LANGUAGES C CXX)

# Store all C/C++ source files into the PROJECT_SOURCE_FILES variable.
# This will recursively search under all directories within ./source.
file(GLOB_RECURSE PROJECT_SOURCE_FILES
	"${PROJECT_SOURCE_DIR}/source/*.c"
	"${PROJECT_SOURCE_DIR}/source/*.cc"
	"${PROJECT_SOURCE_DIR}/source/*.cxx"
	"${PROJECT_SOURCE_DIR}/source/*.cpp"
)

# Store all C/C++ header files into the PROJECT_HEADER_FILES variable.
# This will recursively search under all directories within ./include.
file(GLOB_RECURSE PROJECT_HEADER_FILES
	"${PROJECT_SOURCE_DIR}/include/*.h"
	"${PROJECT_SOURCE_DIR}/include/*.hh"
	"${PROJECT_SOURCE_DIR}/include/*.hxx"
	"${PROJECT_SOURCE_DIR}/include/*.hpp"
)

# Tell the project where to find include files.
include_directories(
	"${PROJECT_SOURCE_DIR}/include"
)

# add_executable(<name> [WIN32] [MACOSX_BUNDLE]
#                [EXCLUDE_FROM_ALL]
#                source1 [source2 ...])
# Name of the executable will be "template".
# The source files are stored in ${Template_SOURCE}.
add_executable(template ${PROJECT_SOURCE_FILES} ${PROJECT_INCLUDE})

# add_library(<name> <SHARED|STATIC|MODULE|UNKNOWN> IMPORTED
#             [GLOBAL])
# If you want to create a library instead of an executable.
#add_library(template SHARED ${PROJECT_SOURCE_FILES}) 
