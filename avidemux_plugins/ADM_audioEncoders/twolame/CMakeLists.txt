INCLUDE(ae_plugin)

SET(ADM_ae_twolame_SRCS audioencoder_twolame.cpp)

ADD_AUDIO_ENCODER(ADM_ae_twolame ${ADM_ae_twolame_SRCS})

TARGET_LINK_LIBRARIES(ADM_ae_twolame PRIVATE "${TWOLAME_LIBRARY_DIR}" )
TARGET_INCLUDE_DIRECTORIES(ADM_ae_twolame PRIVATE "${TWOLAME_INCLUDE_DIR}")


INIT_AUDIO_ENCODER(ADM_ae_twolame)
INSTALL_AUDIOENCODER(ADM_ae_twolame)
