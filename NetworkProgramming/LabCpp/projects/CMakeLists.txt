list(APPEND COMMON_DEPENDENCIES common_utils common_net common_thread common_protocols)

if (WIN32)
    LIST(APPEND COMMON_DEPENDENCIES wsock32 ws2_32)
elseif(LINUX)
    LIST(APPEND COMMON_DEPENDENCIES pthread)
endif()

add_subdirectory(tcp)