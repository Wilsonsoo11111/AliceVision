# Headers
set(mvsUtils_files_headers
  common.hpp
  depthSimMapIO.hpp
  fileIO.hpp
  ImagesCache.hpp
  MultiViewParams.hpp
  TileParams.hpp
)

# Sources
set(mvsUtils_files_sources
  common.cpp
  depthSimMapIO.cpp
  fileIO.cpp
  ImagesCache.cpp
  MultiViewParams.cpp
  TileParams.cpp
)

alicevision_add_library(aliceVision_mvsUtils
  SOURCES ${mvsUtils_files_headers} ${mvsUtils_files_sources}
  PUBLIC_LINKS
    aliceVision_image
    aliceVision_numeric
    aliceVision_multiview
    aliceVision_mvsData
    OpenImageIO::OpenImageIO_Util
  PRIVATE_LINKS
    aliceVision_system
    Boost::filesystem
    Boost::boost
)
