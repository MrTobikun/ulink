cmake_minimum_required(VERSION 3.5)

project(alinker LANGUAGES C)

add_executable(alinker alink.c coff.c cofflib.c combine.c objload.c output.c util.c)
