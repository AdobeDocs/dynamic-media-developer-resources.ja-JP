---
description: ビデオビューア用のコマンドリファレンスドキュメント。
seo-description: ビデオビューア用のコマンドリファレンスドキュメント。
seo-title: コマンドリファレンス — URL
solution: Experience Manager
title: コマンドリファレンス — URL
topic: Dynamic media
uuid: 4f9e4a79-6865-4e41-b30b-84ff2c6f6045
translation-type: tm+mt
source-git-commit: 3266e8682711dac379a09a0e992d33b8ffc7b5a4
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---


# コマンドリファレンス — URL{#command-reference-url}

ビデオビューア用のコマンドリファレンスドキュメント。

URLには任意の設定コマンドを設定できます。 または、APIメソッド`setParam()`、`setParams()`、またはその両方を使用して設定コマンドを設定できます。 サーバー側の設定レコードでconfig属性を指定することもできます。

一部の設定コマンドの先頭に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的で、`setContainerId()` APIメソッドに渡されるビューアコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンドのオプションのプリフィックスが含まれています。 例えば、`playback`は次のように記載されています。

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

これは、このコマンドが次の方法で使用されることを意味します。

* `playback` （短い構文）
* `VideoPlayer.playback` （コンポーネントのクラス名で修飾）
* `cont_videoPlayer.playback` (コンポーネントIDで修飾、コンテナ要素 `cont` のIDとする)

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください。

[すべてのビューアに共通のコマンドリファレンス — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)も参照してください。
