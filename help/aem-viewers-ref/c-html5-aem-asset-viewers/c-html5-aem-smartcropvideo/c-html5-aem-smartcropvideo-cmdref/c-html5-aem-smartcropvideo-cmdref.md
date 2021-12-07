---
title: コマンドリファレンス — 設定属性
description: スマート切り抜きビデオビューアの設定属性ドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: dfd80e5727a128f272855f1f28e1bc89cb2436bf
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

スマート切り抜きビデオビューアの設定属性ドキュメント。

URL 内に任意の設定コマンドを設定できます。 または、 API メソッドを使用できます `setParam()`または `setParams()`またはその両方を指定して、設定コマンドを設定します。 また、サーバー側の設定レコードに任意の設定属性を指定することもできます。

一部の設定コマンドの先頭に、対応するビューア SDK コンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的で、に渡されるビューアのコンテナの DOM 要素の ID に依存します。 `setContainerId()` API メソッド。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例： `playback` は次のように記述されています。

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

つまり、このコマンドは次の方法で使用されます。

* `playback` （短い構文）
* `SmartCropVideoPlayer.playback` （コンポーネントクラス名で修飾）
* `cont_videoPlayer.playback` （コンポーネント ID で修飾、次のように仮定） `cont` はコンテナ要素の ID です )

詳しくは、 [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

詳しくは、 [すべてのビューアに共通のコマンドリファレンス — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
