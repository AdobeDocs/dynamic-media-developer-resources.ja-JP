---
description: Video360ビューアのコマンドリファレンスドキュメント。
solution: Experience Manager
title: コマンドリファレンス — URL
feature: Dynamic Media Classic，ビューア，SDK/API,360 VRビデオ
role: Developer,User
exl-id: eb7026cf-f28b-4426-ba64-b3472946d5d4
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

---

# コマンドリファレンス — URL{#command-reference-url}

Video360ビューアのコマンドリファレンスドキュメント。

URLに任意の設定コマンドを設定できます。 または、APIメソッド`setParam()`、`setParams()`、またはその両方を使用して、任意の設定コマンドを設定できます。 サーバー側の設定レコードに任意の設定属性を指定することもできます。

一部の設定コマンドの先頭に、対応するHTML5ビューアSDKコンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的で、`setContainerId()` APIメソッドに渡されるビューアコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例えば、`playback`は次のように記載されています。

```
[Video360Player.|<containerId>_video360Player].playback
```

これは、このコマンドが次の方法で使用されることを意味します。

* `playback` （短い構文）
* `Video360Player.playback` （コンポーネントクラス名で修飾）
* `cont_video360Player.playback` (コンポーネントIDで修飾、( `cont` はコンテナ要素のID)

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)および[すべてのビューアに共通のコマンドリファレンス — URL](../../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)を参照してください。
