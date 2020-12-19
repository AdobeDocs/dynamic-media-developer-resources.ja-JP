---
description: インタラクティブ画像ビューアの設定属性ドキュメント。
seo-description: インタラクティブ画像ビューアの設定属性ドキュメント。
seo-title: コマンドリファレンス — 設定属性
solution: Experience Manager
title: コマンドリファレンス — 設定属性
topic: Dynamic media
uuid: ef118730-1bd2-4b88-917c-1fa51c6a488b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

インタラクティブ画像ビューアの設定属性ドキュメント。

URL内に任意の設定コマンドを設定するか、`setParam()`、`setParams()`、またはその両方のAPIメソッドを使用して設定できます。 設定属性は、サーバー側の設定レコードでも指定できます。

一部の設定コマンドの先頭に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名のプレフィックスが付く場合があります。 コンポーネントのインスタンス名は動的で、`setContainerId()` APIメソッドに渡されるビューアコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例えば、`zoomstep`コマンドは次のように記載されています。

`[ZoomView.|<containerId>_zoomView].fmt`

これは、このコマンドを次のように使用できることを意味します。

* `fmt` （短い構文）
* `ZoomView.fmt` （コンポーネントのクラス名で修飾）
* `cont_zoomView.fmt` (コンポーネントIDで修飾、ここ `cont` ではコンテナ要素のID)

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください。
