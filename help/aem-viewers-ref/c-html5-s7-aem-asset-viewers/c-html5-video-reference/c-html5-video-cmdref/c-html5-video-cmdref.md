---
description: ビデオビューアの設定属性ドキュメント。
seo-description: ビデオビューアの設定属性ドキュメント。
seo-title: コマンドリファレンス — 設定属性
solution: Experience Manager
title: コマンドリファレンス — 設定属性
topic: Dynamic media
uuid: 837cf230-f7dd-4010-a299-c3267d11e200
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

ビデオビューアの設定属性ドキュメント。

URLには、任意の設定コマンドを設定できます。 または、APIメソッド、またはその両方を使用し `setParam()`て、任意の設 `setParams()`定コマンドを設定することもできます。 サーバー側の設定レコードには、任意のconfig属性を指定することもできます。

一部の設定コマンドの先頭に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名の接頭辞を付けることができます。 コンポーネントのインスタンス名は動的で、 `setContainerId()` APIメソッドに渡されるビューアのコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンドのオプションの接頭辞が含まれています。 例えば、は次のよ `playback` うに記載されています。

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

これは、このコマンドが次の方法で使用されることを意味します。

* `playback` （短い構文）
* `VideoPlayer.playback` （コンポーネントのクラス名で修飾）
* `cont_videoPlayer.playback` (コンポーネントIDで修飾、これ `cont` がコンテナ要素のIDと仮定)

すべてのビ [ューアに共通のコマンドリファレンス — 設定属性を参照してください。](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)

すべてのビ [ューアに共通のコマンドリファレンス — URLを参照してください。](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
