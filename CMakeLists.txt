cmake_minimum_required(VERSION 3.16)

project(ev)

add_library(ev STATIC)
target_include_directories(ev PUBLIC .)
target_sources(ev PRIVATE ev.c event.c)
target_compile_definitions(ev PRIVATE 
    EV_STANDALONE
    EV_FEATURES=0x24
    EV_USE_FLOOR=0
    EV_USE_MONOTONIC=1
    EV_USE_SELECT=1
    EV_USE_POLL=0
    EV_USE_EPOLL=0
    EV_USE_PORT=0
    EV_USE_KQUEUE=0
    EV_USE_INOTIFY=0
    EV_USE_SIGNALFD=0
    EV_USE_EVENTFD=0
    EV_USE_NANOSLEEP=0
    EV_USE_MONOTONIC=1
    EV_USE_CLOCK_SYSCALL=0
    EV_USE_SIGNALFD=0
    EV_USE_EVENTFD=0
)
