project(GMM)

set(GMM_SOURCES
    gmm_main.cpp
    gmm.cpp)
set(GMM_HEADERS
    gmm.h)
set(GMM_LINK_LIBS
    optimized
    opencv_core2410
    optimized
    opencv_highgui2410
    optimized
    opencv_calib3d2410
    optimized
    opencv_imgproc2410
    debug
    opencv_core2410d
    debug
    opencv_highgui2410d
    debug
    opencv_calib3d2410d
    debug
    opencv_imgproc2410d)

include_directories(${OPENCV_INCLUDE})
link_directories(${OPENCV_LIB})

add_executable(GMM
               ${GMM_SOURCES}
               ${GMM_HEADERS})

target_link_libraries(GMM ${GMM_LINK_LIBS})
