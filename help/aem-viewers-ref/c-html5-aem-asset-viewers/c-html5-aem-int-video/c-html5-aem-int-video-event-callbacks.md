---
description: イベントコールバック
solution: Experience Manager
title: イベントコールバック
feature: Dynamic Mediaクラシック，ビューア，SDK/API，インタラクティブビデオ
role: 開発者、業務従事者
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '221'
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
   * `instName {String}` イベントをトリガーしたビューアSDKコンポーネントのインスタンス名。
   * `timeStamp {Number}` イベントのタイムスタンプ。
   * `eventInfo {String}` イベントペイロード。

* `quickViewActivate`  — ユーザがインタラクティブスウォッチコンポーネント内、またはビデオ再生の最後に表示される「行動喚起」画面でインタラクティブスウォッチをクリックまたはタップしたときのトリガー。コールバックハンドラーは、次のフィールドを持つJSONオブジェクトである唯一の引数を受け取ります。

   * `sku` {  `String`}インタラクティブスウォッチに関連付けられているSKU値。
   * `<additionalVariable>` {  `String`}インタラクティブスウォッチに関連付けられた0個以上の追加の変数。

[InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd)および[setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643)も参照してください。
