PROJECT(CsvParser CXX)
ADD_SUBDIRECTORY(src bin)
SET(EXECUTABLE_OUTPUT_PATH ${PROJECT_BINARY_DIR}/)
SET(LIBRARY_OUTPUT_PATH ${PROJECT_BINARY_DIR}/lib)

SET(SRC_LIST src/parse.cpp)

SET(CMAKE_C_FLAGS )
SET(CMAKE_CXX_FLAGS "-std=c++11 -O3 -msse -msse2")
ADD_DEFINITIONS(-DNDEBUG)

MESSAGE(STATUS "This is BIN dir " ${PROJECT_BINARY_DIR})
MESSAGE(STATUS "This is SRC dir " ${PROJECT_SOURCE_DIR})
ADD_EXECUTABLE(CsvParser ${SRC_LIST})

