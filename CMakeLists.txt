cmake_minimum_required(VERSION 3.10)

# Set the title of your project and language
project(PEX0 C)

# Set the version of the C language standard you will be using
set(CMAKE_C_STANDARD 99)

# Turn on helpful compiler warnings
#set(CMAKE_C_FLAGS "-Wall -Werror") # all warnings are on and treated as errors
set(CMAKE_C_FLAGS "-Wall" )

# Settings for use of curses.h
#find_package(curses REQUIRED)
#include_directories(${CURSES_INCLUDE_DIR})
#set(CMAKE_CXX_FLAGS -lcurses)

# Set the source directory, the place where your main.c and
# other files are located (currently not set)
set(SDIR )

# List all files that are required to compile your project
set(SOURCE_FILES
        ${SDIR}pex0.c pex0.h)

# Tell cmake the name of your executable and what source files to
# build from
add_executable(pex0 ${SOURCE_FILES})

# For curses.h
#target_link_libraries(myExe ${CURSES_LIBRARIES})

# For math.h
target_link_libraries(pex0 m)