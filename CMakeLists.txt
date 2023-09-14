cmake_minimum_required(VERSION 3.24)
project(soloudw)

set(CMAKE_CXX_STANDARD 23)
set(LIBRARY_OUTPUT_PATH ${CMAKE_SOURCE_DIR}/lib)
set(SOURCES src/dr_impl.cpp src/soloud.cpp src/soloud_audiosource.cpp src/soloud_bus.cpp src/soloud_core_3d.cpp src/soloud_core_basicops.cpp src/soloud_core_faderops.cpp src/soloud_core_filterops.cpp src/soloud_core_getters.cpp src/soloud_core_setters.cpp src/soloud_core_voicegroup.cpp src/soloud_core_voiceops.cpp src/soloud_fader.cpp src/soloud_fft.cpp src/soloud_fft_lut.cpp src/soloud_file.cpp src/soloud_filter.cpp src/soloud_miniaudio.cpp src/soloud_misc.cpp src/soloud_queue.cpp src/soloud_thread.cpp src/soloud_wav.cpp src/soloud_wavstream.cpp src/stb_vorbis.c)

add_compile_definitions(WITH_MINIAUDIO)
add_library(soloudw ${SOURCES})
target_include_directories(soloudw PRIVATE include/soloudw)
