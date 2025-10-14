---
title: コマンドリファレンス - URL
description: インタラクティブビデオビューアのコマンドリファレンスドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e0a9e269-4826-4518-9222-6a833d11746b
source-git-commit: 6aaf4eccf51a05d200c6cc780e342be646d104d8
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# コマンドリファレンス - URL{#command-reference-url}

インタラクティブビデオビューアのコマンドリファレンスドキュメント。

URL 内の任意の設定コマンドを設定できます。 または、API メソッド `setParam()`、`setParams()`、またはその両方を使用して、任意の設定コマンドを設定できます。 サーバーサイド設定レコードで任意の config 属性を指定することもできます。

一部のコンフィギュレーションコマンドには、対応するビューア SDK コンポーネントのクラス名またはインスタンス名をプレフィックスとして付けることができます。 コンポーネントのインスタンス名は動的であり、API メソッドに渡されるビューアコンテナ DOM 要素の ID`setContainerId()` 依存します。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、`playback` は次のようにドキュメント化されます。

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

つまり、このコマンドは次のように使用されます

* `playback` （短い構文）
* `VideoPlayer.playback` （コンポーネントクラス名で修飾）
* `cont_videoPlayer.playback` （コンポーネント ID で修飾。`cont` はコンテナ要素の ID と仮定）

[&#x200B; すべてのビューアに共通のコマンドリファレンス – 設定属性 &#x200B;](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) も参照してください。

[&#x200B; すべてのビューアに共通のコマンドリファレンス - URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226) も参照してください。
