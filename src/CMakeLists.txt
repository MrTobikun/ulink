cmake_minimum_required(VERSION 3.5)

project(alinker LANGUAGES C)

add_executable(alinker alink.c coff.c cofflib.c combine.c objload.c output.c util.c)

include(../PVS-Studio.cmake)
pvs_studio_add_target(TARGET alinker.analyze ALL
                      OUTPUT FORMAT errorfile
                      ANALYZE ${PROJECT_NAME}
                      MODE GA:1,2 OP
                      LOG target.err)
