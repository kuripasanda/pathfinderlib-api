## PathfinderLib (API)
[PathfinderLib](https://github.com/kuripasanda/PathfinderLib) (プライベートリポジトリ) のAPI部分のコードを公開するためのリポジトリです。

## 使い方
JitPackから依存関係を追加してください。  
```kotlin
repositories {
    maven { url = uri("https://jitpack.io") }
}

dependencies {
    implementation("com.github.kuripasanda:PathfinderLibApi:1.0.2")
}
```
  
KotlinでAPIのインスタンスを取得
```kotlin
var pathfinderLib: PathfinderLibApi? = null

// PathfinderLibのAPIを取得
val loader = FabricLoader.getInstance()
if (loader.isModLoaded(PathfinderLibApi.MOD_ID)) pathfinderLib = loader.objectShare.get("${PathfinderLibApi.MOD_ID}:api") as? PathfinderLibApi
if (pathfinderLib == null) throw IllegalStateException("PathfinderLibが見つかりませんでした。")
```
