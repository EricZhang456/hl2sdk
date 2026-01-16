add_library(hl2sdk_tier1 STATIC
    bitbuf.cpp
    byteswap.cpp
    characterset.cpp
    checksum_crc.cpp
    checksum_md5.cpp
    checksum_sha1.cpp
    commandbuffer.cpp
    convar.cpp
    datamanager.cpp
    diff.cpp
    exprevaluator.cpp
    fileio.cpp
    generichash.cpp
    ilocalize.cpp
    interface.cpp
    KeyValues.cpp
    keyvaluesjson.cpp
    kvpacker.cpp
    lzmaDecoder.cpp
    lzss.cpp
    mempool.cpp
    memstack.cpp
    NetAdr.cpp
    newbitbuf.cpp
    pathmatch.cpp
    qsort_s.cpp
    rangecheckedvar.cpp
    reliabletimer.cpp
    snappy-sinksource.cpp
    snappy-stubs-internal.cpp
    snappy.cpp
    sparsematrix.cpp
    splitstring.cpp
    stringpool.cpp
    strtools.cpp
    strtools_unicode.cpp
    tier1.cpp
    tokenreader.cpp
    undiff.cpp
    uniqueid.cpp
    utlbinaryblock.cpp
    utlbuffer.cpp
    utlbufferutil.cpp
    utlstring.cpp
    utlsymbol.cpp
)

if(LINUX)
    target_sources(hl2sdk_tier1 PRIVATE processor_detect_linux.cpp)
else()
    target_sources(hl2sdk_tier1 PRIVATE processor_detect.cpp)
endif()

target_include_directories(hl2sdk_tier1 PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/../common
    ${CMAKE_CURRENT_SOURCE_DIR}/../public
    ${CMAKE_CURRENT_SOURCE_DIR}/../public/tier0
    ${CMAKE_CURRENT_SOURCE_DIR}/../public/tier1
)

target_compile_definitions(hl2sdk_tier1 PRIVATE WIN32_LEAN_AND_MEAN=)
