cmake_minimum_required(VERSION 3.23)
cmake_policy(VERSION 3.23...3.30)

# Define the Project
project(Awesome VERSION 1.0 LANGUAGES CXX)

set(CPM_DOWNLOAD_VERSION 0.39.0)
# Include the CMake Package Manager
include(cmake/setupCPM.cmake)

# Build our library
add_subdirectory(lib)

# Build our executable
add_subdirectory(bin)

# Build our test
enable_testing()
add_subdirectory(test)

# Configure and Install the Package Config Files
add_subdirectory(cmake)
