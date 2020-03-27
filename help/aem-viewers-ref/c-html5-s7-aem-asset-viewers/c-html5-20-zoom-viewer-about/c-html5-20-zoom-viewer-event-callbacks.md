---
description: 'null'
seo-description: 'null'
seo-title: イベントコールバック
solution: Experience Manager
title: イベントコールバック
topic: Dynamic media
uuid: 325a3ccf-bae9-46f6-b3d0-70041a9548bb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# イベントコールバック{#event-callbacks}

ビューアでは、Webページでビューアの初期化プロセスまたは実行時の動作を追跡する際に使用されるJavaScriptイベントコールバックがサポートされています。

コールバックハンドラーは、イベント名と、プロパティを持つ対応するハンドラー関数を、ビ `handlers` ューアのコンストラク `config` ター内のJSONオブジェクトに渡すことで割り当てられます。 または、 `setHandlers()` APIメソッドを使用できます。

サポートされるビューアイベントは次のとおりです。

* `initComplete`  — ビューアの初期化が完了し、すべての内部コンポーネントが作成されたときにトリガーされ、 `getComponent()` APIを使用できるようになります。 コールバックハンドラーは引数を取りません。

* `trackEvent` - Adobe Analyticsなどのイベント追跡システムで処理可能なイベントがビューア内で発生するたびにトリガーされます。 このコールバックハンドラーは次の引数を取ります。

   * `objID {String}` 現在は使用されていません。
   * `compClass {String}` 現在は使用されていません。
   * `instName {String}` イベントをトリガーしたビューアSDKコンポーネントのインスタンス名。
   * `timeStamp {Number}` イベントのタイムスタンプ。
   * `eventInfo {String}` イベントのペイロード。

ZoomViewerおよび [setHandlersも参照して](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-zoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) ください [](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)。
