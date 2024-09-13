add_subdirectory(hwid_poc_lib)

if(HWID_POC_BUILD_BENCHMARKS)
    add_subdirectory(hwid_poc_benchmark)
endif()
if(HWID_POC_BUILD_TESTS)
    add_subdirectory(hwid_poc_test)
endif()
