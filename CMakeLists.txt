cmake_minimum_required (VERSION 3.0)

project(sslkeylog)

add_library(sslkeylog SHARED sslkeylog.c)

install(TARGETS sslkeylog
    LIBRARY DESTINATION lib)

install(PROGRAMS sslkeylog.py
    DESTINATION bin)