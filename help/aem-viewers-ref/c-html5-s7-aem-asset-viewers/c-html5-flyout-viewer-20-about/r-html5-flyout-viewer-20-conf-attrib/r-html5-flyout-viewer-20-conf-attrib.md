---
title: コマンドリファレンス – 設定属性
description: フライアウトビューアの設定属性に関するドキュメント
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 2ac199ce-5dd5-4d2f-80c2-9bc370500cc4
TQID: 'https://experienceleague.adobe.com/Bus1MH5Y8xppGXxnARx0Fq11dslSbY9Q7yAlFtF6KzI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

フライアウトビューアの設定属性に関するドキュメント

URLで任意の設定コマンドを設定できます。 または、`setParam()`、`setParams()`、またはその両方のAPI メソッドを使用できます。 また、サーバーサイド設定レコードで任意の設定属性を指定することもできます。

一部の設定コマンドには、対応するViewer SDK コンポーネントのクラス名またはインスタンス名が先頭に付きます。 コンポーネントのインスタンス名は動的であり、`setContainerId()` API メソッドに渡されるビューアコンテナ DOM要素のIDによって異なります。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、`zoomfactor` コマンドは次のように文書化されています。

`[FlyoutZoomView.|<containerId>_flyout].zoomfactor`

コマンドは次のように使用されます。

* `zoomfactor` （短い構文）
* `FlyoutZoomView.zoomfactor` （コンポーネントクラス名で修飾）
* `cont_flyout.zoomfactor` （`cont`がコンテナ要素のIDであると仮定すると、コンポーネント IDで修飾されます）

すべてのビューアに共通の[ コマンド参照 – 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください
