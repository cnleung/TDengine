CMAKE_MINIMUM_REQUIRED(VERSION 2.8)
PROJECT(TDengine)

INCLUDE_DIRECTORIES(${TD_COMMUNITY_DIR}/deps/pthread)
INCLUDE_DIRECTORIES(${TD_COMMUNITY_DIR}/deps/iconv)
INCLUDE_DIRECTORIES(${TD_COMMUNITY_DIR}/deps/regex)
INCLUDE_DIRECTORIES(${TD_COMMUNITY_DIR}/src/inc)
INCLUDE_DIRECTORIES(${TD_COMMUNITY_DIR}/src/os/inc)
INCLUDE_DIRECTORIES(${TD_COMMUNITY_DIR}/src/util/inc)
INCLUDE_DIRECTORIES(${TD_COMMUNITY_DIR}/src/common/inc)
AUX_SOURCE_DIRECTORY(. SRC)

ADD_LIBRARY(os ${SRC})

TARGET_LINK_LIBRARIES(os winmm IPHLPAPI ws2_32)
