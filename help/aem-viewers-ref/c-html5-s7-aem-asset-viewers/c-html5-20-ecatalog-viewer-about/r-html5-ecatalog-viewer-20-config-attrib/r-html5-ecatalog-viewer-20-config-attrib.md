---
title: コマンドリファレンス — 設定属性
description: eCatalog ビューアの設定属性ドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

eCatalog ビューアの設定属性ドキュメント。

任意の設定コマンドを URL で設定するか、 `setParam()`または `setParams()`、またはその両方の API メソッド。 また、サーバー側の設定レコードで指定される任意の設定属性を指定することもできます。

一部の設定コマンドでは、対応する Viewer SDK コンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的で、に渡されるビューアのコンテナの DOM 要素の ID に依存します。 `setContainerId()` API メソッド。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例： `zoomstep` コマンドの説明は次のとおりです。

`[PageView.|<containerId>_pageView].zoomstep`

つまり、このコマンドを

* `zoomstep` （短い構文）
* `PageView.zoomstep` （コンポーネントクラス名で修飾）
* `cont_pageView.zoomstep` （コンポーネント ID で修飾、仮定） `cont` はコンテナ要素の ID です )

関連トピック [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
