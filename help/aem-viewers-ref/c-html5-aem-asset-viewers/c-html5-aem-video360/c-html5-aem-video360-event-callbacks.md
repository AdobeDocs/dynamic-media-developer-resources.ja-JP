---
description: イベントコールバック
solution: Experience Manager
title: イベントコールバック
feature: Dynamic Mediaクラシック，ビューア，SDK/API,360 VRビデオ
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 0%

---


# イベントコールバック{#event-callbacks}

ビューアでは、Webページでビューアの初期化プロセスや実行時の動作の追跡に使用されるJavaScriptイベントコールバックがサポートされています。

コールバックハンドラーは、イベント名と`handlers`プロパティを持つ対応するハンドラー関数を、ビューアのコンストラクター内の`config` JSONオブジェクトに渡すことで割り当てられます。 または、`setHandlers()` APIメソッドを使用できます。

サポートされるビューアイベントは次のとおりです。

* `initComplete`  — ビューアの初期化が完了し、すべての内部コンポーネントが作成されたときにトリガーが発生し、 `getComponent()` APIを使用できるようになります。このコールバックハンドラーは引数を取りません。
* `trackEvent` -Adobe Analyticsなどのイベントトラッキングシステムで処理できるイベントがビューア内で発生するたびにトリガーが発生します。このコールバックハンドラーは次の引数を取ります。

   * `objID {String}` 現在は使用されていません。
   * `compClass {String}` 現在は使用されていません。
   * `instName {String}` イベントをトリガーしたHTML5ビューアSDKコンポーネントのインスタンス名。
   * `timeStamp {Number}` イベントのタイムスタンプ。
   * `eventInfo {String}` イベントペイロード。

[Video360Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-video360viewer.md#reference-bd16cadc0c054fafb0db4994741d47cd)および[setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)も参照してください。
