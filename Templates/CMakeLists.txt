project(cpp_snippet)
# cmake_minimum_required(VERSION 3.10)
# set(CMAKE_CXX_STANDARD 17)
# set(CMAKE_SKIP_INSTALL_RULES True)
# set(CMAKE_CXX_FLAGS)

include_directories(include)

## Add build target
set(BIN_TARGET ${CMAKE_PROJECT_NAME}_bin)
file(GLOB SOURCES src/*.cpp)
add_executable(${BIN_TARGET} ${SOURCES})

## Test section
## Note: To enable testing, uncomment the following section and place in the same
##       folder the file CMakeLists.txt.in
## Configure googletest
# configure_file(CMakeLists.txt.in googletest-download/CMakeLists.txt)
# execute_process(COMMAND ${CMAKE_COMMAND} -G "${CMAKE_GENERATOR}" .
#                 WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/googletest-download)
# execute_process(COMMAND ${CMAKE_COMMAND} --build .
#                 WORKING_DIRECTORY ${CMAKE_CURRENT_BINARY_DIR}/googletest-download)
# add_subdirectory(${CMAKE_CURRENT_BINARY_DIR}/googletest-src
#                  ${CMAKE_CURRENT_BINARY_DIR}/googletest-build
#                  EXCLUDE_FROM_ALL)
## Add test target
# include(GoogleTest)
# set(TEST_TARGET ${CMAKE_PROJECT_NAME}_tests)
# file(GLOB TESTS test/*.cpp)
# add_executable(${TEST_TARGET} ${TESTS})
# add_library(target_sources ${SOURCES})
# target_link_libraries(${TEST_TARGET} gtest_main target_sources)
# gtest_discover_tests(${TEST_TARGET} WORKING_DIRECTORY test TEST_PREFIX *_tests:)

