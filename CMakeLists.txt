cmake_minimum_required(VERSION 3.25)

project(exai-cmake VERSION 1.2.0)

include(CMakePackageConfigHelpers)
include(GNUInstallDirs)

write_basic_package_version_file(
  ${CMAKE_CURRENT_BINARY_DIR}/exai-cmake-config-version.cmake
  COMPATIBILITY AnyNewerVersion
)

install(FILES
  ${CMAKE_CURRENT_SOURCE_DIR}/cmake/exai-verilog.cmake
  ${CMAKE_CURRENT_SOURCE_DIR}/cmake/exai-test.cmake
  ${CMAKE_CURRENT_SOURCE_DIR}/exai-cmake-config.cmake
  ${CMAKE_CURRENT_BINARY_DIR}/exai-cmake-config-version.cmake
  DESTINATION ${CMAKE_INSTALL_DATADIR}/exai-cmake
)
