---
description: 'null'
seo-description: 'null'
seo-title: イベントコールバック
solution: Experience Manager
title: イベントコールバック
topic: Dynamic media
uuid: 512f5c08-cf6a-4721-a169-11977cd4c248
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

SpinViewerおよび [setHandlersも参照して](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195) ください [](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef)。
