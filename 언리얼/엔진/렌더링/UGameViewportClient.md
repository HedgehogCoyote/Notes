Input과 Output을 다루는 엔진 객체

Input : 마우스, 키보드(얘네도 OS에서 오긴 함), OS 메세지 등...
Output : Audio, 화면... 

게임 화면이 렌더링 되는 간략한 흐름

`UGameEngine` : GameViewport->Viewport->Draw(bShouldPresent);
`FViewport` : ViewportClient->Draw(this, &Canvas);
`UGameViewportClient` : Draw(FViewport, FCanvas) :
	// 여기 Audio 관련이 있긴한데 View에 따라 어뉴테이션 되는 정도의 의미인 것 같음
	ULocalPlayer들의 [[FSceneView]]를 이용해
	[[FSceneViewFamily]] 를 만들고, 
	GetRendererModule().BeginRenderingViewFamily(SceneCanvas, &ViewFamily)를 호출한다.