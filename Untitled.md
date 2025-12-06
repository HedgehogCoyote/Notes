들을 걸 듣는다
BindOnActorInitStateChanged(UPawnExtensionComponent::NAME_ActorFeatureName, FGameplayTag(), true);


bool UPawnInputManagerComponent::CanChangeInitState(UGameFrameworkComponentManager* Manager, FGameplayTag CurrentState, FGameplayTag DesiredState) const

-> 여기서 '내가 바꿀 상태인지 체크'

HandleChangeInitState(UGameFrameworkComponentManager* Manager,  FGameplayTag CurrentState, FGameplayTag DesiredState)