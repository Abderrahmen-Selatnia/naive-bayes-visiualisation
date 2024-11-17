cmake_minimum_required(VERSION 3.10)

# Set the project name and version
project(NaiveBayes VERSION 1.0 DESCRIPTION "An SDL Project" LANGUAGES C)


# Enable C11 or later standard
set(CMAKE_C_STANDARD 11)

# Find SDL2
find_package(SDL2 REQUIRED)

# Include SDL2 headers
include_directories(${SDL2_INCLUDE_DIRS})
include_directories(${CMAKE_SOURCE_DIR}/include)

# Add your source files
add_executable(NaiveBayes
    src/main.c
    src/ali_hamo.c
    src/fadel_abderrahmen.c
)

# Link SDL2 to the project
target_link_libraries(NaiveBayes ${SDL2_LIBRARIES})

# Ensure CMake can find SDL2 in non-standard locations (if needed)
set(SDL2_DIR ${CMAKE_SOURCE_DIR}/include/SDL2)

# For Windows, you might need additional specific libraries or flags.
if(WIN32)
    # Windows-specific SDL setup, e.g., linking static libraries or defining additional flags
    target_link_libraries(NaiveBayes SDL2main SDL2)
    # Adjust include and library paths if SDL2 is not installed globally on Windows
    include_directories(${CMAKE_SOURCE_DIR}/include/SDL2)
    link_directories(${CMAKE_SOURCE_DIR}/src/SDL2)
endif()

# Optional: Set the output directories for the build
set(CMAKE_ARCHIVE_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_LIBRARY_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/lib)
set(CMAKE_RUNTIME_OUTPUT_DIRECTORY ${CMAKE_BINARY_DIR}/bin)
