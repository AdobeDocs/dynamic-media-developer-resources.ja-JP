---
description: ビデオ360ビューアのコマンドリファレンスドキュメント。
seo-description: ビデオ360ビューアのコマンドリファレンスドキュメント。
seo-title: コマンドリファレンス — URL
solution: Experience Manager
title: コマンドリファレンス — URL
topic: Dynamic media
uuid: 70c212d7-35ee-408f-abe4-19ba1e4d773d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# コマンドリファレンス — URL{#command-reference-url}

ビデオ360ビューアのコマンドリファレンスドキュメント。

URLには、任意の設定コマンドを設定できます。 または、APIメソッド、またはその両方を使用し `setParam()`て、任意の設 `setParams()`定コマンドを設定することもできます。 サーバー側の設定レコードには、任意のconfig属性を指定することもできます。

一部の設定コマンドの先頭に、対応するHTML5ビューアSDKコンポーネントのクラス名またはインスタンス名の接頭辞を付けることができます。 コンポーネントのインスタンス名は動的で、 `setContainerId()` APIメソッドに渡されるビューアのコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンドのオプションの接頭辞が含まれています。 例えば、は次のよ `playback` うに記載されています。

```
[Video360Player.|<containerId>_video360Player].playback
```

これは、このコマンドが次の方法で使用されることを意味します。

* `playback` （短い構文）
* `Video360Player.playback` （コンポーネントのクラス名で修飾）
* `cont_video360Player.playback` (コンポーネントIDで修飾、これ `cont` がコンテナ要素のIDと仮定)

すべてのビ [ューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) 、およびすべ [てのビューアに共通のコマンドリファレンス — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)
