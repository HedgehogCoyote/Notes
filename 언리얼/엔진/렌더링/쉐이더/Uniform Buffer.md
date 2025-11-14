상수 데이터들을 넣는 곳
ViewMatrix, Color 등... 
```
// 구조화된 데이터 블록 BEGIN_UNIFORM_BUFFER_STRUCT(FMyUniformBuffer, )
	SHADER_PARAMETER(FMatrix, WorldMatrix) 
	SHADER_PARAMETER(FVector4, Color) 
END_UNIFORM_BUFFER_STRUCT() 

// 셰이더에서 사용 LAYOUT_FIELD(TUniformBufferRef<FMyUniformBuffer>, MyUniformBuffer)
```