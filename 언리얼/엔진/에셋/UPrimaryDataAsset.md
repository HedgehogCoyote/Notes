UAssetManager가 인지하는 에셋, 

```
UCLASS() class UWeaponData : public UPrimaryDataAsset 
{ 
GENERATED_BODY() 
public: 

UPROPERTY(EditAnywhere) 
float Damage; 

UPROPERTY(EditAnywhere, AssetBundles="InGame") TSoftObjectPtr<UTexture2D> Icon; 

UPROPERTY(EditAnywhere, AssetBundles="Cinematic") TSoftObjectPtr<USkeletalMesh> HighQualityMesh; 

};
```

AssetBundle 메타데이터를 이용해서 원하는 번들로만 로드 가능

```
UAssetManager::Get().LoadPrimaryAsset( FPrimaryAssetId("Weapon", "Sword"), {"InGame"});
```