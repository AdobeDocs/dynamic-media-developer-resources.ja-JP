---
title: コマンドリファレンス - URL
description: スマート切り抜きビデオビューアのコマンドリファレンスドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: d0797c10-2379-45f7-9e8d-a5eb56638db8
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# コマンドリファレンス - URL{#command-reference-url}

スマート切り抜きビデオビューアのコマンドリファレンスドキュメント。

URL 内の任意の設定コマンドを設定できます。 または、API メソッド `setParam()`、`setParams()`、またはその両方を使用して、任意の設定コマンドを設定できます。 サーバーサイド設定レコードで任意の config 属性を指定することもできます。

一部のコンフィギュレーションコマンドには、対応するビューア SDK コンポーネントのクラス名またはインスタンス名をプレフィックスとして付けることができます。 コンポーネントのインスタンス名は動的であり、API メソッドに渡されるビューアコンテナ DOM 要素の ID`setContainerId()` 依存します。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、`playback` は次のようにドキュメント化されます。

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

つまり、このコマンドは次のように使用されます。

* `playback` （短い構文）
* `SmartCropVideoPlayer.playback` （コンポーネントクラス名で修飾）
* `cont_smartCropVideoPlayer.playback` （コンポーネント ID で修飾。`cont` はコンテナ要素の ID と仮定）

[&#x200B; すべてのビューアに共通のコマンドリファレンス – 設定属性 &#x200B;](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) も参照してください。

[&#x200B; すべてのビューアに共通のコマンドリファレンス - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) も参照してください。
