cmake_minimum_required(VERSION 3.10)
project(sctp C)

set(CMAKE_C_STANDARD 99)

IF(CMAKE_SYSTEM_NAME MATCHES "Darwin")
    INCLUDE_DIRECTORIES (
            /usr/local/include/glib-2.0
            /usr/local/lib/glib-2.0/include
    )
ELSE() #linux

ENDIF()


add_library(sctp STATIC
        adaptation.c
        auxiliary.c
        chunkHandler.c
        distribution.c
        errorhandler.c
        flowcontrol.c globals.c
        md5.c
        pathmanagement.c
        rbundling.c
        recvctrl.c
        reltransfer.c
        sbundling.c
        SCTP-control.c
        streamengine.c
        timer_list.c)