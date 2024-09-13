file(GLOB_RECURSE HWID_POC_SOURCE_CPP
    CONFIGURE_DEPENDS
    ${CMAKE_CURRENT_LIST_DIR}/*.cpp
)

add_library(libhwid_poc STATIC ${HWID_POC_SOURCE_CPP})
target_include_directories(libhwid_poc PUBLIC ${CMAKE_CURRENT_LIST_DIR})
