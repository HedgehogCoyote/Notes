```
// 텍스처, 버퍼 등의 GPU 리소스
SHADER_PARAMETER_TEXTURE(Texture2D, MyTexture)
SHADER_PARAMETER_SAMPLER(SamplerState, MySampler)
SHADER_PARAMETER_RDG_BUFFER_UAV(RWBuffer<float>, OutputBuffer)
SHADER_PARAMETER_SRV(StructuredBuffer<float>, InputBuffer)
```