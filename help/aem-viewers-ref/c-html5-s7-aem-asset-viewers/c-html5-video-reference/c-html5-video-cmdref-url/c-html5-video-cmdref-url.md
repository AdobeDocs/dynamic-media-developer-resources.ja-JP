---
description: ビデオビューアのコマンドリファレンスドキュメント。
seo-description: ビデオビューアのコマンドリファレンスドキュメント。
seo-title: コマンドリファレンス — URL
solution: Experience Manager
title: コマンドリファレンス — URL
topic: Dynamic media
uuid: 4f9e4a79-6865-4e41-b30b-84ff2c6f6045
translation-type: tm+mt
source-git-commit: 3266e8682711dac379a09a0e992d33b8ffc7b5a4

---


# コマンドリファレンス — URL{#command-reference-url}

ビデオビューアのコマンドリファレンスドキュメント。

URLには、任意の設定コマンドを設定できます。 または、APIメソッド、またはその両方を使用し `setParam()`て、任意の設 `setParams()`定コマンドを設定することもできます。 サーバー側の設定レコードには、任意のconfig属性を指定することもできます。

一部の設定コマンドの先頭に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名の接頭辞を付けることができます。 コンポーネントのインスタンス名は動的で、 `setContainerId()` APIメソッドに渡されるビューアのコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンドのオプションの接頭辞が含まれています。 例えば、は次のよ `playback` うに記載されています。

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

これは、このコマンドが次の方法で使用されることを意味します。

* `playback` （短い構文）
* `VideoPlayer.playback` （コンポーネントのクラス名で修飾）
* `cont_videoPlayer.playback` (コンポーネントIDで修飾、これ `cont` がコンテナ要素のIDと仮定)

すべてのビューアに共 [通のコマンドリファレンス — 設定属性も参照してください](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)。

すべてのビューア [に共通のコマンドリファレンス — URLも参照してください](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)。
