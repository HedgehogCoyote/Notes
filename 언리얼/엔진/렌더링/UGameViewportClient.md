Input과 Output을 다루는 엔진 객체

Input : 마우스, 키보드(얘네도 OS에서 오긴 함), OS 메세지 등...
Output : Audio, 화면... 

UGameEngine: GameViewport->Viewport->Draw(bShouldPresent);
`FViewport` ViewportClient->Draw(this, &Canvas);
Draw(FViewport, FCanvas) :
ULocalPlayer들의 [[FSceneView]]를 이용해
[[FSceneViewFamily]] 를 만들고, 
GetRendererModule().BeginRenderingViewFamily(SceneCanvas, &ViewFamily)를 호출한다.