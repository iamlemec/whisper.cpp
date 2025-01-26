if (WHISPER_SDL2)
    set(TARGET whisper-logger)
    add_executable(${TARGET} logger.cpp)

    include(DefaultTargetOptions)

    target_link_libraries(${TARGET} PRIVATE common common-sdl whisper ${CMAKE_THREAD_LIBS_INIT})

    install(TARGETS ${TARGET} RUNTIME)
endif ()
