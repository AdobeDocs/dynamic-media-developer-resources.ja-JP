---
title: コマンドリファレンス – 設定属性
description: Flyout ビューアの設定属性に関するドキュメント
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 15e7881f-ec4f-4e44-9833-1cf965800760
source-git-commit: 50dddf148345d2ca5243d5d7108fefa56d23dad6
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

Flyout ビューアの設定属性に関するドキュメント

URL で任意の設定コマンドを設定できます。 または、`setParam()`、`setParams()`、またはその両方の API メソッドを使用できます。 サーバーサイド設定レコードで任意の設定属性を指定することもできます。

一部の設定コマンドには、対応する Viewer SDK コンポーネントのクラス名またはインスタンス名のプレフィックスが付きます。 コンポーネントのインスタンス名は動的であり、API メソッドに渡されるビューアコンテナ DOM 要素の ID`setContainerId()` 依存します。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、`zoomfactor` コマンドは次のように記述されています。

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

コマンドは次のように使用します。

* `zoomfactor` （短い構文）
* `FlyoutZoomView.zoomfactor` （コンポーネントクラス名で修飾）
* `cont_flyout.zoomfactor` （コンポーネント ID で修飾。`cont` はコンテナ要素の ID と仮定）

[ すべてのビューアに共通のコマンドリファレンス – 設定属性 ](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) も参照してください。
