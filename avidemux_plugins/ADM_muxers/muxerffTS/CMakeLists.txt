include(mx_plugin)
SET(ADM_ffTS_SRCS
 muxerffTS.cpp
 muxerffTSPlugin.cpp
        muxerffTSConfig.cpp
)

ADD_MUXER(ADM_mx_ffTS ${ADM_ffTS_SRCS})

TARGET_LINK_LIBRARIES(ADM_mx_ffTS  PRIVATE ADM_libavutil ADM_libavcodec ADM_libavformat)
INIT_MUXER(ADM_mx_ffTS)
INSTALL_MUXER(ADM_mx_ffTS)

