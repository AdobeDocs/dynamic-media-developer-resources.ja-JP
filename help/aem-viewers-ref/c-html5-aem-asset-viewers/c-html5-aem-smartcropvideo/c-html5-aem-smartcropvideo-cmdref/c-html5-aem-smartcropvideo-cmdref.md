---
title: コマンドリファレンス – 設定属性
description: スマート切り抜きビデオビューアの設定属性ドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
mini-toc-levels: 3
exl-id: 698c03b1-bec0-44bf-9c79-c66e0192344a
source-git-commit: eaf59166fcc1ff8ec5a2e846ef0eb180c8cbdd5a
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---


# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

スマート切り抜きビデオビューアの設定属性ドキュメント。

URL 内の任意の設定コマンドを設定できます。 または、API メソッド `setParam()`、`setParams()`、またはその両方を使用して、任意の設定コマンドを設定できます。 サーバーサイド設定レコードで任意の config 属性を指定することもできます。

一部の設定コマンドには、対応する Viewer SDK コンポーネントのクラス名またはインスタンス名をプレフィックスとして付けることができます。 コンポーネントのインスタンス名は動的であり、API メソッドに渡されるビューアコンテナ DOM 要素の ID`setContainerId()` 依存します。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、`playback` は次のようにドキュメント化されます。

```
[SmartCropVideoPlayer.|<containerId>_smartCropVideoPlayer].playback
```

つまり、このコマンドは次のように使用されます。

* `playback` （短い構文）
* `SmartCropVideoPlayer.playback` （コンポーネントクラス名で修飾）
* `cont_videoPlayer.playback` （コンポーネント ID で修飾。`cont` はコンテナ要素の ID と仮定）

[ すべてのビューアに共通のコマンドリファレンス – 設定属性 ](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) を参照してください。

[ すべてのビューアに共通のコマンドリファレンス - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) を参照してください。
