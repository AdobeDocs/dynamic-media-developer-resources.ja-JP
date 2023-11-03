---
title: コマンドリファレンス — 設定属性
description: 混在メディアビューアの設定属性ドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aa750941-0a2e-4591-bdff-5e71ecc342aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

混在メディアビューアの設定属性ドキュメント。

任意の設定コマンドを URL で設定するか、 `setParam()`または `setParams()`またはその両方の API メソッドを使用できます。 設定属性は、サーバー側の設定レコードでも指定できます。

一部の設定コマンドの前に、対応する Viewer SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付く場合があります。 コンポーネントのインスタンス名は動的で、に渡されるビューアのコンテナの DOM 要素の ID に依存します。 `setContainerId()` API メソッド。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例： `zoomstep` コマンドの説明は次のとおりです。

`[ZoomView.|<containerId>_zoomView].zoomstep`

つまり、次のように、このコマンドを使用できます。

* `zoomstep` （短い構文）
* `ZoomView.zoomstep` （コンポーネントのクラス名で修飾）
* `cont_zoomView.zoomstep` （コンポーネント ID で修飾、仮定） `cont` はコンテナ要素の ID です )

関連トピック [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
