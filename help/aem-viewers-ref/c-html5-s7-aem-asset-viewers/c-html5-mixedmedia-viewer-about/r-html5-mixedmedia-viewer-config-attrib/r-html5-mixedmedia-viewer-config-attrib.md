---
title: コマンドリファレンス – 設定属性
description: Mixed Media Viewerの設定属性に関するドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: aa750941-0a2e-4591-bdff-5e71ecc342aa
TQID: 'https://experienceleague.adobe.com/7s8EFmP3YkVcrk2kMi35mXMrffw1GQQTmXTwvWWGVnc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 145
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

Mixed Media Viewerの設定属性に関するドキュメント。

任意の設定コマンドは、URLまたは`setParam()`、`setParams()`、またはその両方のAPI メソッドを使用して設定できます。 任意のconfig属性をサーバーサイド設定レコードで指定することもできます。

一部の設定コマンドには、対応するViewer SDK コンポーネントのクラス名またはインスタンス名が先頭に付いている場合があります。 コンポーネントのインスタンス名は動的であり、`setContainerId()` API メソッドに渡されるビューアコンテナ DOM要素のIDによって異なります。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、`zoomstep` コマンドは次のように文書化されています。

`[ZoomView.|<containerId>_zoomView].zoomstep`

つまり、このコマンドを次のように使用できます

* `zoomstep` （短い構文）
* `ZoomView.zoomstep` （コンポーネントクラス名で修飾）
* `cont_zoomView.zoomstep` （`cont`がコンテナ要素のIDであると仮定して、コンポーネント IDで修飾）

すべてのビューアに共通の[ コマンド参照 – 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください
