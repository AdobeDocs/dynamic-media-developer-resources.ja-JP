---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 14b317ab-82fb-4f55-babe-72c24e6afc2c
TQID: 'https://experienceleague.adobe.com/GEH2LfIdpNqG-PuOObYC0BHtfetkMJDIf32HCEmP9u4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
ht-degree: 0%

---

# イベントコールバック{#event-callbacks}

ビューアは、Web ページがビューアの初期化プロセスまたはランタイム動作をトラッキングするために使用するJavaScript イベントコールバックをサポートしています。

コールバックハンドラーは、`handlers` プロパティを持つイベント名と対応するハンドラー関数をビューアのコンストラクターの`config` JSON オブジェクトに渡すことによって割り当てられます。 または、`setHandlers()` API メソッドを使用することもできます。

サポートされるビューアイベントには、次のものがあります。

* `initComplete` - ビューアの初期化が完了し、すべての内部コンポーネントが作成されたときにトリガーが発生します。これにより、`getComponent()` APIを使用できます。 コールバックハンドラーは引数を受け取りません。

* `trackEvent` - Adobe Analyticsなどのイベントトラッキングシステムで処理できるビューア内でイベントが発生するたびにトリガーします。 コールバックハンドラーは次の引数を取ります。

   * `objID {String}`は現在使用されていません。
   * `compClass {String}`は現在使用されていません。
   * `instName {String}` イベントをトリガーしたViewer SDK コンポーネントのインスタンス名。
   * `timeStamp {Number}` イベントタイムスタンプ。
   * `eventInfo {String}` イベントペイロード。

[BasicZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-basiczoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd)および[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-b748b29eaafa463a9d1723cb7b86f0d9)も参照してください。
