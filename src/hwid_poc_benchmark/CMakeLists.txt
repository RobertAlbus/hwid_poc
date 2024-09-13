file(GLOB_RECURSE HWID_POC_BENCHMARK_SOURCE_CPP
    CONFIGURE_DEPENDS
    ${CMAKE_CURRENT_LIST_DIR}/*.cpp
)

add_executable(hwid_poc_benchmark ${HWID_POC_BENCHMARK_SOURCE_CPP})
target_include_directories(hwid_poc_benchmark PUBLIC ${CMAKE_CURRENT_LIST_DIR})

target_link_libraries(hwid_poc_benchmark PUBLIC benchmark::benchmark libhwid_poc)