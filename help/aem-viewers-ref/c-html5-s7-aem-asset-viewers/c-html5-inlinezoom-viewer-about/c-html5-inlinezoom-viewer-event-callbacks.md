---
description: イベントコールバック
solution: Experience Manager
title: イベントコールバック
feature: Dynamic Media Classic，ビューア，SDK/API，インラインズーム
role: Developer,Business Practitioner
exl-id: c54c54ae-f98f-4cd4-8c36-c7e2a9f3c6df
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '155'
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

[FlyoutViewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-.flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e)および[setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692)も参照してください。
