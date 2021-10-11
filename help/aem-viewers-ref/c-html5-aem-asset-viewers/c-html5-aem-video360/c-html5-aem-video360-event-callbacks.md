---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 24ea35c0-a0b1-4768-9336-94eb5e2d4fb2
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# イベントコールバック{#event-callbacks}

ビューアでは、Web ページでビューアの初期化プロセスや実行時の動作の追跡に使用される JavaScript イベントコールバックがサポートされています。

コールバックハンドラーを割り当てるには、イベント名と `handlers` プロパティを持つ対応するハンドラー関数を、ビューアのコンストラクター内の `config` JSON オブジェクトに渡します。 または、`setHandlers()` API メソッドを使用することもできます。

サポートされるビューアイベントは次のとおりです。

* `initComplete`  — ビューアの初期化が完了し、すべての内部コンポーネントが作成されたら、API を使用できるように `getComponent()` します。コールバックハンドラーは引数を取りません。
* `trackEvent` - Adobe Analyticsなどのイベントトラッキングシステムで処理できるイベントがビューア内で発生するたびにトリガーされます。コールバックハンドラーは次の引数を取ります。

   * `objID {String}` 現在は使用されていません。
   * `compClass {String}` 現在は使用されていません。
   * `instName {String}` イベントをトリガーしたHTML5 ビューア SDK コンポーネントのインスタンス名。
   * `timeStamp {Number}` イベントのタイムスタンプ。
   * `eventInfo {String}` イベントペイロード。

[Video360Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-video360viewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) および [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643) も参照してください。
