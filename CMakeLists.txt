cmake_minimum_required(VERSION 3.1)
project(game.libretro.gambatte)

list(APPEND CMAKE_MODULE_PATH ${PROJECT_SOURCE_DIR})

find_package(Kodi REQUIRED)
find_package(libretro-gambatte REQUIRED)

set(DEPLIBS gambatte)
set(GAMBATTE_CUSTOM_BINARY ${GAMBATTE_LIB}
                           ${PROJECT_NAME}${CMAKE_SHARED_LIBRARY_SUFFIX})

build_addon(${PROJECT_NAME} GAMBATTE DEPLIBS)
