add_library(hl2sdk_mathlib STATIC
    3dnow.cpp
    almostequal.cpp
    anorms.cpp
    bumpvects.cpp
    color_conversion.cpp
    halton.cpp
    IceKey.cpp
    imagequant.cpp
    lightdesc.cpp
    mathlib_base.cpp
    polyhedron.cpp
    powsse.cpp
    quantize.cpp
    randsse.cpp
    simdvectormatrix.cpp
    sparse_convolution_noise.cpp
    spherical.cpp
    sse.cpp
    sseconst.cpp
    ssenoise.cpp
    vector.cpp
    vmatrix.cpp
)

target_include_directories(hl2sdk_mathlib PRIVATE
    ${CMAKE_CURRENT_SOURCE_DIR}/../public
    ${CMAKE_CURRENT_SOURCE_DIR}/../public/tier0
    ${CMAKE_CURRENT_SOURCE_DIR}/../public/mathlib
)
