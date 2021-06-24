---
description: フライアウトビューアの設定属性に関するドキュメント
solution: Experience Manager
title: コマンドリファレンス — 設定属性
feature: Dynamic Media Classic，ビューア，SDK/API，インラインズーム
role: Developer,Business Practitioner
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

フライアウトビューアの設定属性に関するドキュメント

URLに任意の設定コマンドを設定できます。 または、`setParam()`、`setParams()`、または両方のAPIメソッドを使用できます。 サーバー側の設定レコードで任意の設定属性を指定することもできます。

一部の設定コマンドの前に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名が付きます。 コンポーネントのインスタンス名は動的で、`setContainerId()` APIメソッドに渡されるビューアコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例えば、`zoomfactor`コマンドは次のように記述されています。

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

コマンドは次のように使用します。

* `zoomfactor` （短い構文）
* `FlyoutZoomView.zoomfactor` （コンポーネントクラス名で修飾）
* `cont_flyout.zoomfactor` (コンポーネントIDで修飾、( `cont` はコンテナ要素のID)

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください。
