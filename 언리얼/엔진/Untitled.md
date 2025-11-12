```
int32 GaurdedMain(const TCHAR* CmdLine) 
{
	EngineInit();
	
	while(!IsEngineExitRequested())
	{
		EngineTick();
	}
	
	
}
```