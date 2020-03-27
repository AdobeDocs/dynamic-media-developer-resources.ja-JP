---
description: eCatalogビューアの設定属性ドキュメント。
seo-description: eCatalogビューアの設定属性ドキュメント。
seo-title: コマンドリファレンス — 設定属性
solution: Experience Manager
title: コマンドリファレンス — 設定属性
topic: Dynamic media
uuid: 823ad411-653a-44de-97de-147e3b27a917
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

eCatalogビューアの設定属性ドキュメント。

設定コマンドはURLで設定することも、APIメソッドを使用するこ `setParam()`とも、APIメソッドを `setParams()`使用することも、両方使用することもできます。 サーバー側の設定レコードで指定された設定属性を指定することもできます。

一部の設定コマンドでは、対応するビューアSDKコンポーネントのクラス名またはインスタンス名の接頭辞を付けることができます。 コンポーネントのインスタンス名は動的で、 `setContainerId()` APIメソッドに渡されるビューアのコンテナのDOM要素のIDに依存します。 このようなコマンドのオプションのプレフィックスがドキュメントに含まれています。 例えば、コマンドは `zoomstep` 次のように記載されています。

`[PageView.|<containerId>_pageView].zoomstep`

つまり、このコマンドは次のように使用できます。

* `zoomstep` （短い構文）
* `PageView.zoomstep` （コンポーネントのクラス名で修飾）
* `cont_pageView.zoomstep` (コンポーネントIDで修飾、 `cont` はコンテナ要素のIDとする)

すべてのビューアに共 [通のコマンドリファレンス — 設定属性も参照してください。](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
