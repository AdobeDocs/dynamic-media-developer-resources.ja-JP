---
title: コマンドリファレンス — 設定属性
description: スピンビューアの設定属性ドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 60615258-4d20-4452-a4a3-94fb88a943d7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# コマンドリファレンス — 設定属性{#command-reference-configuration-attributes}

スピンビューアの設定属性ドキュメント。

任意の設定コマンドを URL で設定するか、 `setParam()`または `setParams()`またはその両方の API メソッドを使用できます。 設定属性は、サーバー側の設定レコードでも指定できます。

一部の設定コマンドの前に、対応するビューア SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付く場合があります。 コンポーネントのインスタンス名は動的で、に渡されるビューアのコンテナの DOM 要素の ID に依存します。 `setContainerId()` API メソッド。 ドキュメントには、このようなコマンド用のオプションのプレフィックスが含まれています。 例： `zoomstep` コマンドの説明は次のとおりです。

`[SpinView.|<containerId>_spinView].zoomstep`

つまり、次のように、このコマンドを使用できます。

* `zoomstep` （短い構文）
* `SpinView.zoomstep` （コンポーネントのクラス名で修飾）
* `cont_spinView.zoomstep` （コンポーネント ID で修飾、仮定） `cont` はコンテナ要素の ID です )

関連トピック [すべてのビューアに共通のコマンドリファレンス — 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)
