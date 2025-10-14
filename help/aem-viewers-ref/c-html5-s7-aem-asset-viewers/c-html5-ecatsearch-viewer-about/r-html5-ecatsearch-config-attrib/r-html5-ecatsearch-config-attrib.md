---
description: eCatalog ビューアの設定属性ドキュメント。
solution: Experience Manager
title: コマンドリファレンス – 設定属性
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

eCatalog ビューアの設定属性ドキュメント。

設定コマンドは、URL で設定することも、`setParam()`、`setParams()`、またはその両方の API メソッドを使用して設定することもできます。 サーバーサイド設定レコードで指定された任意の設定属性を指定することもできます。

一部の設定コマンドでは、対応するビューア SDK コンポーネントのクラス名またはインスタンス名をプレフィックスとして指定できます。 コンポーネントのインスタンス名は動的であり、API メソッドに渡されるビューアコンテナ DOM 要素の ID`setContainerId()` 依存します。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、次 `zoomstep` コマンドはドキュメントに記載されています。

`[PageView.|<containerId>_pageView].zoomstep`

つまり、このコマンドは次のように使用できます。

* `zoomstep` （短い構文）
* `PageView.zoomstep` （コンポーネントクラス名で修飾）
* `cont_pageView.zoomstep` （コンポーネント ID で修飾。`cont` はコンテナ要素の ID と仮定）

[&#x200B; すべてのビューアに共通のコマンドリファレンス – 設定属性 &#x200B;](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) も参照してください。
