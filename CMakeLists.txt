CMAKE_MINIMUM_REQUIRED(VERSION 2.8.12)

ADD_COMPILE_OPTIONS($<$<CXX_COMPILER_ID:MSVC>:/MP>)

PROJECT(helper)

SET(DEPENDENCIES_DIR CACHE PATH "")
SET(QT_ROOT CACHE PATH "")

# hint to find qt in dependencies path
LIST(APPEND CMAKE_PREFIX_PATH ${QT_ROOT}/lib/cmake)

ADD_SUBDIRECTORY(src)