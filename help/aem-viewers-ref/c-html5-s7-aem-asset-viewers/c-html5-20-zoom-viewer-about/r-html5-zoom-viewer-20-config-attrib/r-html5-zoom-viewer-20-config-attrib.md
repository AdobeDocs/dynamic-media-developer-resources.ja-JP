---
title: コマンドリファレンス – 設定属性
description: Zoom Viewerの設定属性に関するドキュメント。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 03982627-9298-4032-a15a-a5afe4ec1fb5
TQID: 'https://experienceleague.adobe.com/34VqWl1GOWOG7G8vXJIpc7NH4w26x2NOGO3yG2yknyc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f6432244ef9faba7a81488e9de8e438154ae6123
workflow-type: tm+mt
source-wordcount: 141
ht-degree: 0%

---

# コマンドリファレンス – 設定属性{#command-reference-configuration-attributes}

Zoom Viewerの設定属性に関するドキュメント。

任意の設定コマンドは、URLまたは`setParam()`、`setParams()`、またはその両方のAPI メソッドを使用して設定できます。 任意のconfig属性をサーバーサイド設定レコードで指定することもできます。

一部の設定コマンドには、対応するViewer SDK コンポーネントのクラス名またはインスタンス名が先頭に付いている場合があります。 コンポーネントのインスタンス名は動的であり、`setContainerId()` API メソッドに渡されるビューアコンテナ DOM要素のIDによって異なります。 ドキュメントには、このようなコマンドのオプションのプレフィックスが含まれています。 例えば、`zoomstep` コマンドは次のように文書化されています。

`[ZoomView.|<containerId>_zoomView].zoomstep`

つまり、コマンドを次のように使用できます

* `zoomstep` （短い構文）
* `ZoomView.zoomstep` （コンポーネントクラス名で修飾）
* `cont_zoomView.zoomstep` （`cont`がコンテナ要素のIDであると仮定して、コンポーネント IDで修飾）

すべてのビューアに共通の[ コマンド参照 – 設定属性](../../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd)も参照してください

