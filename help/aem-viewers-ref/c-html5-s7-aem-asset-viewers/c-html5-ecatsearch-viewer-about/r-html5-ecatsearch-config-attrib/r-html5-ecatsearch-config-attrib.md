---
description: eCatalogビューアの設定属性ドキュメント。
seo-description: eCatalogビューアの設定属性ドキュメント。
seo-title: コマンドリファレンス — 設定属性
solution: Experience Manager
title: コマンドリファレンス — 設定属性
topic: Dynamic media
uuid: e1111ce2-67e8-449a-9cc2-bb53b61158a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---


# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

eCatalogビューアの設定属性ドキュメント。

URL内に任意の設定コマンドを設定するか、`setParam()`、`setParams()`、またはその両方のAPIメソッドを使用して設定できます。 サーバー側の設定レコードで指定された設定属性を指定することもできます。

一部の設定コマンドの前に、対応するビューアSDKコンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的で、`setContainerId()` APIメソッドに渡されるビューアコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、`zoomstep`コマンドは次のように記載されています。

`[PageView.|<containerId>_pageView].zoomstep`

これは、このコマンドを次のように使用できることを意味します。

* `zoomstep` （短い構文）
* `PageView.zoomstep` （コンポーネントのクラス名で修飾）
* `cont_pageView.zoomstep` (コンポーネントIDで修飾、ここ `cont` ではコンテナ要素のID)

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください。
