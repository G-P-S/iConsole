cmake_minimum_required(VERSION 2.8)
list(APPEND CMAKE_MODULE_PATH ${GOPRO_TOOLS_DIR}/cmake)
include("${GOPRO_TOOLS_DIR}/cmake/gopro.cmake")

gopro_init(iConsole)
gopro_begin_lib(iConsole GROUP 3rdparty)
gopro_include_dirs(GTM)
gopro_public_include_dirs(iConsole)
gopro_files(DIR iConsole GROUP src
    iConsole.m
)
gopro_public_files(DIR iConsole INSTALL_DIR public_include
    iConsole.h
)
gopro_files(DIR GTM GROUP src/GTM
    GTMStackTrace.m
)
gopro_files(DIR GTM GROUP include/GTM
    GTMStackTrace.h
)
gopro_end_lib()

