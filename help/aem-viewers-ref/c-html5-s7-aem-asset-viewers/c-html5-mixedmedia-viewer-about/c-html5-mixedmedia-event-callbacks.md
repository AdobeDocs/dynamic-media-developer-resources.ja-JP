---
description: 'null'
seo-description: 'null'
seo-title: イベントコールバック
solution: Experience Manager
title: イベントコールバック
topic: Dynamic media
uuid: 696838d2-11e4-4ef8-9cd3-136c5d5f6ed9
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

MixedMediaViewerおよび [setHandlersも参照してく](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195) ださい [](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3)。
