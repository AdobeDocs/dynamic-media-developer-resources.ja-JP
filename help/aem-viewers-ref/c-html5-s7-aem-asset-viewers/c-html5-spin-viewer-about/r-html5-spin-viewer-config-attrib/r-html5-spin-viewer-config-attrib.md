---
title: コマンドリファレンス – 設定属性
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

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

スピンビューアの設定属性ドキュメント。

設定コマンドは、URL で設定することも、`setParam()`、`setParams()`、またはその両方の API メソッドを使用して設定することもできます。 サーバーサイド設定レコードでは、任意の config 属性も指定できます。

一部の設定コマンドには、対応するビューア SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付いているものがあります。 コンポーネントのインスタンス名は動的であり、API メソッドに渡されるビューアコンテナ DOM 要素の ID`setContainerId()` 依存します。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、次 `zoomstep` コマンドはドキュメントに記載されています。

`[SpinView.|<containerId>_spinView].zoomstep`

つまり、このコマンドは次のように使用できます

* `zoomstep` （短い構文）
* `SpinView.zoomstep` （コンポーネントクラス名で修飾）
* `cont_spinView.zoomstep` （コンポーネント ID で修飾。`cont` はコンテナ要素の ID と仮定）

[&#x200B; すべてのビューアに共通のコマンドリファレンス – 設定属性 &#x200B;](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) も参照してください。
