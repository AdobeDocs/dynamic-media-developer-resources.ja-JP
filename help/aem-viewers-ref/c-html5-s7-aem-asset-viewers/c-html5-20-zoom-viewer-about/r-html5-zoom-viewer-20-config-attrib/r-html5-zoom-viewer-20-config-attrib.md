---
title: コマンドリファレンス – 設定属性
description: ズームビューアの設定属性ドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

ズームビューアの設定属性ドキュメント。

設定コマンドは、URL で設定することも、`setParam()`、`setParams()`、またはその両方の API メソッドを使用して設定することもできます。 サーバーサイド設定レコードでは、任意の config 属性も指定できます。

一部の設定コマンドには、対応する Viewer SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付いているものがあります。 コンポーネントのインスタンス名は動的であり、API メソッドに渡されるビューアコンテナ DOM 要素の ID`setContainerId()` 依存します。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、次 `zoomstep` コマンドはドキュメントに記載されています。

`[ZoomView.|<containerId>_zoomView].zoomstep`

つまり、コマンドを次のように使用できます

* `zoomstep` （短い構文）
* `ZoomView.zoomstep` （コンポーネントクラス名で修飾）
* `cont_zoomView.zoomstep` （コンポーネント ID で修飾。`cont` はコンテナ要素の ID と仮定）

[ すべてのビューアに共通のコマンドリファレンス – 設定属性 ](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) も参照してください。
