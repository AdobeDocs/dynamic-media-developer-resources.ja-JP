---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7bd2e167-d04c-43e2-a71c-e2b3dddb13a0
TQID: 'https://experienceleague.adobe.com/IUEkVoGiS2GLGbA9XBpYW3fyaE-oK9BaBEDxFgsZoFA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
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
   * `eventInfo {String}` イベントペイロード

[eCatalogViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-ecatalogviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd)および[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856)も参照してください。
