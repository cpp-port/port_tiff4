cmake_minimum_required(VERSION 3.16)
project(tiff4 CXX)


if (MSVC)
    set(CMAKE_DEBUG_POSTFIX "d")
    add_definitions(-D_CRT_SECURE_NO_DEPRECATE)
    add_definitions(-D_CRT_NONSTDC_NO_DEPRECATE)
    include_directories(${CMAKE_CURRENT_SOURCE_DIR})
endif ()


list(APPEND library_source
        mkg3states.c
        mkspans.c
        PluginTIFF.c
        resource.h
        ThomasBS.txt
        tif_config.vc.h
        tif_predict.c
        tif_write.c
        tif_jbig.c
        tif_fax3.c
        tif_dir.c
        tif_dirread.c
        tif_open.c
        tif_color.c
        tif_config.wince.h
        tif_pixarlog.c
        tif_tile.c
        tif_config.h
        tif_swab.c
        tif_print.c
        tif_luv.c
        tif_win32.c
        tif_dirwrite.c
        tif_predict.h
        tif_getimage.c
        tif_lzma.c
        tif_zip.c
        tif_next.c
        tif_compress.c
        tif_dir.h
        tif_unix.c
        tif_version.c
        tif_thunder.c
        tif_strip.c
        tif_dumpmode.c
        tif_config.h-vms
        tif_flush.c
        tif_dirinfo.c
        tif_otiff4.c
        tif_stream.cxx
        tif_warning.c
        tif_wince.c
        tif_vms.c
        tif_read.c
        tif_error.c
        tif_extension.c
        tif_tiff4_12.c
        tif_lzw.c
        tif_fax3.h
        tif_aux.c
        tif_tiff4.c
        tif_fax3sm.c
        tif_close.c
        tiff.h
        tif_packbits.c
        t4.h
        tif_codec.c
        tif_config.h.in
        mkg3states.c
        mkspans.c
        PluginTIFF.c
        resource.h
        ThomasBS.txt
        tif_config.vc.h
        tif_predict.c
        tif_write.c
        tif_jbig.c
        tif_fax3.c
        tif_dir.c
        tif_dirread.c
        tif_open.c
        tif_color.c
        tif_config.wince.h
        tif_pixarlog.c
        tif_tile.c
        tif_config.h
        tif_swab.c
        tif_print.c
        tif_luv.c
        tif_win32.c
        tif_dirwrite.c
        tif_predict.h
        tif_getimage.c
        tif_lzma.c
        tif_zip.c
        tif_next.c
        tif_compress.c
        tif_dir.h
        tif_unix.c
        tif_version.c
        tif_thunder.c
        tif_strip.c
        tif_dumpmode.c
        tif_config.h-vms
        tif_flush.c
        tif_dirinfo.c
        tif_otiff4.c
        tif_stream.cxx
        tif_warning.c
        tif_wince.c
        tif_vms.c
        tif_read.c
        tif_error.c
        tif_extension.c
        tif_tiff4_12.c
        tif_lzw.c
        tif_fax3.h
        tif_aux.c
        tif_tiff4.c
        tif_fax3sm.c
        tif_close.c
        tiff.h
        tif_packbits.c
        t4.h
        tif_codec.c
        tiffio.h
        uvcode.h
        tiffvers.h
        tiffio.hxx
        tiffiop.h
        tiffconf.h
)


add_library(${PROJECT_NAME} SHARED ${library_source})


target_compile_definitions(${PROJECT_NAME} PRIVATE OPJ_EXPORTS)


target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR})
target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/..)
target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../webp)
target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../jxr/common)
target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/include/FreeImage)
target_include_directories(${PROJECT_NAME} PRIVATE ${CMAKE_CURRENT_SOURCE_DIR}/../../../operating_system/operating_system-${OPERATING_SYSTEM_LOWERED_NAME}/configuration/FreeImage)



