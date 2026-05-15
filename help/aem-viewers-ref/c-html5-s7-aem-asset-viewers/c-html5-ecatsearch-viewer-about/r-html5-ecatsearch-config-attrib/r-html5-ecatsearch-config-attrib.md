---
description: eCatalog Viewerの設定属性に関するドキュメント。
solution: Experience Manager
title: コマンドリファレンス – 設定属性
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: e8ce40c9-d1c0-454f-b8fa-ba19e3fe2091
TQID: 'https://experienceleague.adobe.com/S8ZeVKc8YwkQUC1rMsG24BtgHkFdXtWZzKYJMXnm61w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

eCatalog Viewerの設定属性に関するドキュメント。

任意の設定コマンドは、URLまたは`setParam()`、`setParams()`、またはその両方のAPI メソッドを使用して設定できます。 また、サーバーサイド設定レコードで指定されている任意の設定属性を指定することもできます。

一部のコンフィギュレーションコマンドでは、対応するViewer SDK コンポーネントのクラス名またはインスタンス名のプレフィックスを付けることができます。 コンポーネントのインスタンス名は動的であり、`setContainerId()` API メソッドに渡されるビューアコンテナ DOM要素のIDによって異なります。 ドキュメントには、そのようなコマンドのオプションのプレフィックスが含まれています。 例えば、`zoomstep` コマンドは次のように文書化されています。

`[PageView.|<containerId>_pageView].zoomstep`

つまり、このコマンドを次のように使用できます。

* `zoomstep` （短い構文）
* `PageView.zoomstep` （コンポーネントクラス名で修飾）
* `cont_pageView.zoomstep` （`cont`がコンテナ要素のIDであると仮定して、コンポーネント IDで修飾）

すべてのビューアに共通の[&#x200B; コマンド参照 – 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください
