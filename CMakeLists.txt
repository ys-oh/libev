
zephyr_library_named(libev)

if (CONFIG_LIBEV)
zephyr_include_directories(.)
zephyr_sources(ev.c event.c)
zephyr_compile_definitions(
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

zephyr_library_link_libraries(posix_subsys)

endif()
