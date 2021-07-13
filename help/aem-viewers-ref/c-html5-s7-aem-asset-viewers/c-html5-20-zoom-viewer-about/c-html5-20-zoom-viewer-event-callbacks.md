---
description: イベントコールバック
solution: Experience Manager
title: イベントコールバック
feature: Dynamic Media Classic，ビューア，SDK/API，ズーム
role: Developer,User
exl-id: 68aa55da-5f6f-4c7d-8d3f-c25de9cc325c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# イベントコールバック{#event-callbacks}

ビューアでは、Webページでビューアの初期化プロセスや実行時の動作の追跡に使用されるJavaScriptイベントコールバックがサポートされています。

コールバックハンドラーを割り当てるには、イベント名と`handlers`プロパティを持つ対応するハンドラー関数を、ビューアのコンストラクター内の`config` JSONオブジェクトに渡します。 または、`setHandlers()` APIメソッドを使用することもできます。

サポートされるビューアイベントは次のとおりです。

* `initComplete` - APIを使用できるように、ビューアの初期化が完了し、すべての内部コンポーネントが作成されたときにトリガーさ `getComponent()` れます。コールバックハンドラーは引数を取りません。

* `trackEvent` - Adobe Analyticsなどのイベントトラッキングシステムで処理できるイベントがビューア内で発生するたびにトリガーされます。コールバックハンドラーは次の引数を取ります。

   * `objID {String}` 現在は使用されていません。
   * `compClass {String}` 現在は使用されていません。
   * `instName {String}` イベントをトリガーしたビューアSDKコンポーネントのインスタンス名。
   * `timeStamp {Number}` イベントのタイムスタンプ。
   * `eventInfo {String}` イベントペイロード。

[ZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-zoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd)および[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)も参照してください。
