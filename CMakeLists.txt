cmake_minimum_required (VERSION 2.6)
project (JSON)
# The version number.
set (JSON_VERSION_MAJOR 1)
set (JSON_VERSION_MINOR 0)
 

include_directories("${JSON_BINARY_DIR}")
include_directories(${JSON_SOURCE_DIR}/Sources)
include_directories(${JSON_SOURCE_DIR}/Headers)
include_directories(${JSON_BINARY_DIR}/Sources)
include_directories(${JSON_BINARY_DIR}/Headers)
 
SET (JSON_SOURCES
   jsonFile.cxx
   json.cpp)
 
SET (JSON_HEADERS
   jsonFile.h
   json.hpp
)

ADD_DEFINITIONS(
    -std=c++11 # Or -std=c++0x
    # Other flags
)

# add the executable
add_executable(JSON  ${JSON_SOURCES} ${JSON_HEADERS} )

MESSAGE(${JSON_SOURCE_DIR}/)
MESSAGE(${CMAKE_CURRENT_SOURCE_DIR}/)
