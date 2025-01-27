# SPDX-License-Identifier: Apache-2.0

cmake_minimum_required(VERSION 3.20.0)

find_package(Zephyr REQUIRED HINTS $ENV{ZEPHYR_BASE})
project(hello_world)


set(CMAKE_EXPORT_COMPILE_COMMANDS ON)

target_sources(app PRIVATE
    src/analogConfigTbl_NFC08A1.c
    src/demo_ce.c
    src/demo_polling.c
    src/main.c
    )

set(extra_includes
            "src"
            )

target_include_directories(app PUBLIC ${extra_includes})
