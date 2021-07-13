---
description: ビデオビューアの設定属性ドキュメント。
solution: Experience Manager
title: コマンドリファレンス — 設定属性
feature: Dynamic Media Classic，ビューア，SDK/API，ビデオ
role: Developer,User
exl-id: 5992e5cd-7783-408e-a23f-fdcc3a3d6b69
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

ビデオビューアの設定属性ドキュメント。

URLに任意の設定コマンドを設定できます。 または、APIメソッド`setParam()`、`setParams()`、またはその両方を使用して、任意の設定コマンドを設定できます。 サーバー側の設定レコードに任意の設定属性を指定することもできます。

一部の設定コマンドの先頭に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的で、`setContainerId()` APIメソッドに渡されるビューアコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例えば、`playback`は次のように記載されています。

```
[VideoPlayer.|<containerId>_videoPlayer].playback
```

これは、このコマンドが次の方法で使用されることを意味します。

* `playback` （短い構文）
* `VideoPlayer.playback` （コンポーネントクラス名で修飾）
* `cont_videoPlayer.playback` (コンポーネントIDで修飾、( `cont` はコンテナ要素のID)

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)を参照してください。

[すべてのビューアに共通のコマンドリファレンス — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。
