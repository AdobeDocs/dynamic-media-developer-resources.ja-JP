---
description: フライアウトビューアの設定属性ドキュメント
seo-description: フライアウトビューアの設定属性ドキュメント
seo-title: コマンドリファレンス — 設定属性
solution: Experience Manager
title: コマンドリファレンス — 設定属性
topic: Dynamic media
uuid: d7e89a24-a235-4f20-86d1-25aacd118880
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---


# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

フライアウトビューアの設定属性ドキュメント

設定コマンドはURL内に設定できます。 または、`setParam()`、`setParams()`、または両方のAPIメソッドを使用できます。 サーバー側の設定レコードに任意の設定属性を指定することもできます。

一部の設定コマンドの先頭に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名のプレフィックスが付けられます。 コンポーネントのインスタンス名は動的で、`setContainerId()` APIメソッドに渡されるビューアコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例えば、`zoomfactor`コマンドは次のように記載されています。

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

このコマンドは次のように使用します。

* `zoomfactor` （短い構文）
* `FlyoutZoomView.zoomfactor` （コンポーネントのクラス名で修飾）
* `cont_flyout.zoomfactor` (コンテナ要素のIDと仮定して、コンポーネントID `cont` で修飾)

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください。
