---
description: イベントコールバック
solution: Experience Manager
title: イベントコールバック
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: 1a7b51c1-baa7-4ae3-b6b7-17478055a605
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '156'
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

[MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195)および[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3)も参照してください。
