들을 걸 듣는다
BindOnActorInitStateChanged(UPawnExtensionComponent::NAME_ActorFeatureName, FGameplayTag(), true);

TryToChangeInitState(ParadoxGameplayTag::InitializeState_JustSpawned);로 일단스폰 됐음으로 바꿈 

bool UPawnInputManagerComponent::CanChangeInitState(UGameFrameworkComponentManager* Manager, FGameplayTag CurrentState, FGameplayTag DesiredState) const (알아서 호출 됨)

-> 여기서 '내가 바꿀 상태인지 체크'
-> 밑에꺼 호출 
실제 내가 뭘 해야하는지 정의(알아서 호출됨)
HandleChangeInitState(UGameFrameworkComponentManager* Manager,  FGameplayTag CurrentState, FGameplayTag DesiredState)

// 듣고 있음 이벤트를
OnActorInitStateChanged(const FActorInitStateChangedParams& Params)

여기서 
void UPawnInputManagerComponent::CheckDefaultInitialization()를 호출함 // State Chain 을 정의

는

`ContinueInitStateChain(StateChain)` 를 호출 함 얘는 CanChangeInitState를 확인하고, HandleChangeInitState를 호출 하는 것 같음 ( 추정)