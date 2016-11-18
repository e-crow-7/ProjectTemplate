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

add_custom_target(gcc echo hello)

# Will search through the project "src" directory for cpp files.
file(GLOB PROJECT_SOURCE
	"${PROJECT_SOURCE_DIR}/src/*.cpp"
)

# Check the available compilers and add custom targets.
# If Clang is available.
if (CMAKE_CXX_COMPILER_ID MATCHES "Clang")

endif()
# If GNU GCC is available.
if (CMAKE_CXX_COMPILER_ID MATCHES "GNU")

endif()
# If Intel C++ Compiler is available.
if (CMAKE_CXX_COMPILER_ID MATCHES "Intel")

endif()
# If Visual Studio C++ is available.
if (CMAKE_CXX_COMPILER_ID MATCHES "MSVC")

endif()

# add_executable(<name> [WIN32] [MACOSX_BUNDLE]
#                [EXCLUDE_FROM_ALL]
#                source1 [source2 ...])
# Name of the executable will be "template".
# The source files are stored in ${Template_SOURCE}.
add_executable(template ${PROJECT_SOURCE})
