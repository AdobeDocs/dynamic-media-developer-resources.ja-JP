---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '154'
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
   * `eventInfo {String}` イベントペイロード。

関連トピック [SmartCropVideoViewer]
(/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md) および [setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md).
