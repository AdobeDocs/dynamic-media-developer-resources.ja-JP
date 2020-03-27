---
description: 'null'
seo-description: 'null'
seo-title: イベントコールバック
solution: Experience Manager
title: イベントコールバック
topic: Dynamic media
uuid: d98074f1-7dd9-4a7f-9ef8-ebd47b698869
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

FlyoutViewerおよび [setHandlersも参照して](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-.flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e) ください [](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692)。
