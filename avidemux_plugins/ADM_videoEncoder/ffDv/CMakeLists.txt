INCLUDE(ve_plugin)

SET(ffDv_SRCS
        ffDvPlugin.cpp
        ADM_ffDv.cpp
)

ADD_VIDEO_ENCODER(ADM_ve_ffDv  ${ffDv_SRCS})

TARGET_INCLUDE_DIRECTORIES(ADM_ve_ffDv PRIVATE ${CMAKE_CURRENT_BINARY_DIR})
INIT_VIDEO_ENCODER(ADM_ve_ffDv)
INSTALL_VIDEO_ENCODER(ADM_ve_ffDv)
TARGET_LINK_LIBRARIES(ADM_ve_ffDv PRIVATE ADM_libavcodec ADM_libavutil)
INCLUDE_DIRECTORIES("${AVIDEMUX_SOURCE_DIR}/avidemux/")
