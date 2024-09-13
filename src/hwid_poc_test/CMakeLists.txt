find_program(HWID_POC_CTEST_EXECUTABLE ctest)
if(NOT HWID_POC_CTEST_EXECUTABLE)
    message(FATAL_ERROR "ctest not found!")
endif()

# set(CMAKE_CTEST_ARGUMENTS "")

file(GLOB_RECURSE HWID_POC_SOURCE_CPP
    CONFIGURE_DEPENDS
    ${CMAKE_CURRENT_LIST_DIR}/*.cpp
)

add_executable(hwid_poc_test ${HWID_POC_SOURCE_CPP})
target_link_libraries(hwid_poc_test PRIVATE libhwid_poc GTest::gtest GTest::gtest_main)

add_test(NAME hwid_poc_test COMMAND hwid_poc_test)
