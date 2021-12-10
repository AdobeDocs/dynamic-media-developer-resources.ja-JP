---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 68aa55da-5f6f-4c7d-8d3f-c25de9cc325c
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# イベントコールバック{#event-callbacks}

ビューアでは、Web ページでビューアの初期化処理または実行時の動作の追跡に使用される JavaScript イベントコールバックがサポートされています。

コールバックハンドラーは、イベント名と対応するハンドラー関数を `handlers` プロパティを `config` ビューアのコンストラクター内の JSON オブジェクト。 または、 `setHandlers()` API メソッド。

サポートされるビューアイベントには、次のものがあります。

* `initComplete`  — ビューアの初期化が完了し、すべての内部コンポーネントが作成されたときにトリガーが発生し、 `getComponent()` API コールバックハンドラーは引数を取りません。

* `trackEvent` - Adobe Analyticsなどのイベントトラッキングシステムで処理できるビューア内でイベントが発生するたびにトリガーされます。 コールバックハンドラーは次の引数を取ります。

   * `objID {String}` 現在は使用されていません。
   * `compClass {String}` 現在は使用されていません。
   * `instName {String}` イベントをトリガーしたビューア SDK コンポーネントのインスタンス名。
   * `timeStamp {Number}` イベントのタイムスタンプ。
   * `eventInfo {String}` イベントペイロード

関連トピック [ZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-zoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) および [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
