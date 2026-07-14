---
title: コマンドリファレンス – 設定属性
description: eCatalog Viewerの設定属性に関するドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: d15061db-8941-44aa-b90d-598c1ce58a67
TQID: 'https://experienceleague.adobe.com/NRcFJ2RyskUxLayfdSmJ-jk-rHjPWiOWt0XwQJ7tvM8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

eCatalog Viewerの設定属性に関するドキュメント。

任意の設定コマンドは、URLまたは`setParam()`、`setParams()`、またはその両方のAPI メソッドを使用して設定できます。 また、サーバーサイド設定レコードで指定されている任意の設定属性を指定することもできます。

一部のコンフィギュレーションコマンドでは、対応するViewer SDK コンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的であり、`setContainerId()` API メソッドに渡されるビューアコンテナ DOM要素のIDによって異なります。 ドキュメントには、そのようなコマンドのオプションのプレフィックスが含まれています。 例えば、`zoomstep` コマンドは次のように文書化されています。

`[PageView.|<containerId>_pageView].zoomstep`

つまり、このコマンドを

* `zoomstep` （短い構文）
* `PageView.zoomstep` （コンポーネントクラス名で修飾）
* `cont_pageView.zoomstep` （`cont`がコンテナ要素のIDであると仮定して、コンポーネント IDで修飾）

すべてのビューアに共通の[&#x200B; コマンド参照 – 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください

