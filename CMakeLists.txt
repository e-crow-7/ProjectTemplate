# Using functionality present in the 3.0.2 CMake documentation.
cmake_minimum_required (VERSION 3.0.2)

# project(<PROJECT-NAME>
#        [VERSION <major>[.<minor>[.<patch>[.<tweak>]]]]
#		 [LANGUAGES <language-name>...])
# The project's name is "Template".
# Set version is 1 Major and 0 Minor.
# This project uses C and CXX (CXX = C++) languages.
project(Template VERSION 1.0 LANGUAGES C CXX)


file(GLOB PROJECT_SOURCE
	"${PROJECT_SOURCE_DIR}/src/*.cpp"
)

# add_executable(<name> [WIN32] [MACOSX_BUNDLE]
#                [EXCLUDE_FROM_ALL]
#                source1 [source2 ...])
# Name of the executable will be "template".
# The source files are stored in ${Template_SOURCE}.
add_executable(template ${PROJECT_SOURCE})
