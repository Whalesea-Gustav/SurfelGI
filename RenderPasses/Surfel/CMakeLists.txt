add_plugin(Surfel)

target_sources(Surfel PRIVATE
    SurfelBase.cpp

    Random.hlsli
    SurfelTypes.hlsli
    SurfelUtils.hlsli

    SurfelGBuffer/SurfelGBuffer.cpp
    SurfelGBuffer/SurfelGBuffer.h
    SurfelGBuffer/SurfelGBuffer.3d.slang

    SurfelPreparePass/SurfelPreparePass.cpp
    SurfelPreparePass/SurfelPreparePass.h
    SurfelPreparePass/SurfelPreparePass.hlsl

    SurfelUpdatePass/SurfelUpdatePass.cpp
    SurfelUpdatePass/SurfelUpdatePass.h
    SurfelUpdatePass/SurfelUpdatePass.hlsl

    SurfelCoveragePass/SurfelCoveragePass.cpp
    SurfelCoveragePass/SurfelCoveragePass.h
    SurfelCoveragePass/SurfelCoveragePass.hlsl

    SurfelGenPass/SurfelGenPass.cpp
    SurfelGenPass/SurfelGenPass.h
    SurfelGenPass/SurfelGenPass.hlsl
)

target_copy_shaders(Surfel RenderPasses/Surfel)

target_source_group(Surfel "RenderPasses")
