cmake_minimum_required(VERSION 3.5)
project(isolated_vad_c)

set(CMAKE_CXX_FLAGS "${CMAKE_CXX_FLAGS} -std=c++11")
add_definitions(-DWEBRTC_POSIX)
set(SOURCE_FILES main.c webrtc/common_audio/vad/webrtc_vad.c
        webrtc/common_audio/vad/vad_core.c
        webrtc/common_audio/vad/vad_filterbank.c
        webrtc/common_audio/vad/vad_gmm.c
        webrtc/common_audio/vad/vad_sp.c
        webrtc/common_audio/signal_processing/spl_init.c
        webrtc/common_audio/signal_processing/division_operations.c
        webrtc/common_audio/signal_processing/resample_48khz.c
        webrtc/common_audio/signal_processing/energy.c
        webrtc/common_audio/signal_processing/resample.c
        webrtc/common_audio/signal_processing/resample_by_2.c
        webrtc/common_audio/signal_processing/resample_fractional.c
        webrtc/common_audio/signal_processing/resample_by_2_internal.c
        webrtc/common_audio/signal_processing/spl_sqrt.c
        webrtc/common_audio/signal_processing/sqrt_of_one_minus_x_squared.c
        webrtc/common_audio/signal_processing/vector_scaling_operations.c
        webrtc/common_audio/signal_processing/real_fft.c
        webrtc/common_audio/signal_processing/get_scaling_square.c
        webrtc/common_audio/signal_processing/downsample_fast.c
        webrtc/common_audio/signal_processing/complex_fft.c
        webrtc/common_audio/signal_processing/cross_correlation.c
        webrtc/common_audio/signal_processing/complex_bit_reverse.c
        webrtc/common_audio/signal_processing/min_max_operations.c)
add_executable(isolated_vad_c ${SOURCE_FILES})