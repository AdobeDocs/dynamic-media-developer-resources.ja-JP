---
description: eCatalogビューアの設定属性ドキュメント。
solution: Experience Manager
title: コマンドリファレンス — 設定属性
feature: Dynamic Media Classic，ビューア，SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

eCatalogビューアの設定属性ドキュメント。

設定コマンドは、URLまたは`setParam()`、`setParams()`、またはその両方のAPIメソッドを使用して設定できます。 サーバー側の設定レコードで指定された任意の設定属性を指定することもできます。

一部の設定コマンドでは、対応するビューアSDKコンポーネントのクラス名またはインスタンス名の前にを付けることができます。 コンポーネントのインスタンス名は動的で、`setContainerId()` APIメソッドに渡されるビューアコンテナのDOM要素のIDに依存します。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例えば、`zoomstep`コマンドは次のように記述されています。

`[PageView.|<containerId>_pageView].zoomstep`

つまり、このコマンドは次のように使用できます。

* `zoomstep` （短い構文）
* `PageView.zoomstep` （コンポーネントクラス名で修飾）
* `cont_pageView.zoomstep` (コンポーネントIDで修飾、 `cont` はコンテナ要素のID)

[すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください。
