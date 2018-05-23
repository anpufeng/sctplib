CMAKE_MINIMUM_REQUIRED (VERSION 3.5)


PROJECT (programs)

IF(CMAKE_SYSTEM_NAME MATCHES "Darwin")
    set(lib_dep sctp glib-2.0)
ELSE() #linux

ENDIF()

add_executable(chargen_server chargen_server.c)
target_link_libraries(chargen_server ${lib_dep})

add_executable(chat chat.c)
target_link_libraries(chat ${lib_dep})

add_executable(combined_server combined_server.c)
target_link_libraries(combined_server ${lib_dep})

add_executable(daytime_server daytime_server.c)
target_link_libraries(daytime_server ${lib_dep})

add_executable(discard_server discard_server.c)
target_link_libraries(discard_server ${lib_dep})

add_executable(echo_monitor echo_monitor.c)
target_link_libraries(echo_monitor ${lib_dep})

add_executable(echo_server echo_server.c)
target_link_libraries(echo_server ${lib_dep})

add_executable(echo_tool echo_tool.c)
target_link_libraries(echo_tool ${lib_dep})

add_executable(localcom localcom.c)
target_link_libraries(localcom ${lib_dep})

add_executable(main main.c)
target_link_libraries(main ${lib_dep})

add_executable(mini-ulp mini-ulp.c)
target_link_libraries(mini-ulp ${lib_dep})

add_executable(monitor monitor.c)
target_link_libraries(monitor ${lib_dep})

add_executable(parser parser.c)
target_link_libraries(parser ${lib_dep})

add_executable(sctptest parser.c)
target_link_libraries(sctptest ${lib_dep})

add_executable(terminal terminal.c)
target_link_libraries(terminal ${lib_dep})

add_executable(test_tool test_tool.c)
target_link_libraries(test_tool ${lib_dep})

add_executable(testengine testengine.c)
target_link_libraries(testengine ${lib_dep})

add_executable(testsctp testsctp.c sctp_wrapper.c)
target_link_libraries(testsctp ${lib_dep})

