cmake_minimum_required (VERSION 3.0)

project(sslkeylog)

add_library(sslkeylog SHARED sslkeylog.c)

set_target_properties(sslkeylog PROPERTIES
    VERSION 1.0.0
    SOVERSION 1)

install(TARGETS sslkeylog
    LIBRARY DESTINATION lib)

install(PROGRAMS sslkeylog.py
    DESTINATION bin)