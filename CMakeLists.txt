cmake_minimum_required(VERSION 3.2)
project(json5pp VERSION 2.3.0 LANGUAGES CXX)

add_library(tinyformat INTERFACE)

include(GNUInstallDirs)

install(TARGETS tinyformat EXPORT tinyformatConfig)
install(FILES ${CMAKE_CURRENT_SOURCE_DIR}/tinyformat/tinyformat.h DESTINATION ${CMAKE_INSTALL_INCLUDEDIR}/tinyformat)
install(EXPORT tinyformatConfig DESTINATION lib/tinyformat)

