option(HWID_POC_FETCH_DEPENDENCIES     "" ON)
option(HWID_POC_FETCH_GOOGLE_BENCHMARK "FetchContent for Google Benchmark" ON)
option(HWID_POC_FETCH_GOOGLE_TEST      "FetchContent for Google Test"      ON)

message("\n\n== Dependencies ==\n")

message("HWID_POC_FETCH_DEPENDENCIES:     ${HWID_POC_FETCH_DEPENDENCIES}")
message("HWID_POC_FETCH_GOOGLE_BENCHMARK: ${HWID_POC_FETCH_GOOGLE_BENCHMARK}")
message("HWID_POC_FETCH_GOOGLE_TEST:      ${HWID_POC_FETCH_GOOGLE_TEST}")

include(GoogleBenchmark.cmake)
include(GoogleTest.cmake)
message("\n--------\n")

