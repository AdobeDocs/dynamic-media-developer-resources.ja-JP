---
description: 'null'
seo-description: 'null'
seo-title: イベントコールバック
solution: Experience Manager
title: イベントコールバック
topic: Dynamic media
uuid: b9252d4b-cff1-42eb-9e56-553091f854b5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---


# イベントコールバック{#event-callbacks}

ビューアでは、Webページでビューアの初期化プロセスや実行時の動作の追跡に使用されるJavaScriptイベントコールバックがサポートされています。

コールバックハンドラーは、イベント名と`handlers`プロパティを持つ対応するハンドラー関数を、ビューアのコンストラクター内の`config` JSONオブジェクトに渡すことで割り当てられます。 または、`setHandlers()` APIメソッドを使用できます。

サポートされるビューアイベントは次のとおりです。

* `initComplete`  — ビューアの初期化が完了し、すべての内部コンポーネントが作成され、 `getComponent()` APIを使用できるようになったときにトリガーされます。このコールバックハンドラーは引数を取りません。
* `trackEvent` -Adobe Analyticsなどのイベントトラッキングシステムで処理できるイベントがビューア内で発生するたびにトリガーされます。このコールバックハンドラーは次の引数を取ります。

   * `objID {String}` 現在は使用されていません。
   * `compClass {String}` 現在は使用されていません。
   * `instName {String}` イベントをトリガーしたビューアSDKコンポーネントのインスタンス名。
   * `timeStamp {Number}` イベントのタイムスタンプ。
   * `eventInfo {String}` イベントペイロード。

* `quickViewActivate`  — ユーザがインタラクティブスウォッチコンポーネント内、またはビデオ再生の最後に表示される「行動喚起」画面でインタラクティブスウォッチをクリックまたはタップしたときにトリガーされます。コールバックハンドラーは、次のフィールドを持つJSONオブジェクトである唯一の引数を受け取ります。

   * `sku` {  `String`}インタラクティブスウォッチに関連付けられているSKU値。
   * `<additionalVariable>` {  `String`}インタラクティブスウォッチに関連付けられた0個以上の追加の変数。

[InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd)および[setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)も参照してください。
