---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2493208b-9030-49fa-b1fd-2f2bd524bce6
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# イベントコールバック{#event-callbacks}

ビューアは、JavaScript イベントコールバックをサポートしています。このコールバックは、web ページで、ビューアの初期化プロセスやランタイムの動作のトラッキングに使用されます。

コールバックハンドラーは、`handlers` プロパティを持つイベント名と対応するハンドラー関数をビューアのコンストラクター内 `config`JSON オブジェクトに渡すことによって割り当てられます。 または、API メソッドを使用するこ `setHandlers()` もできます。

次のビューアイベントがサポートされています。

* `initComplete` - ビューアの初期化が完了し、すべての内部コンポーネントが作成されて API を使用できるようになっ `getComponent()` ときのトリガー。 コールバックハンドラーは引数を取りません。

* `trackEvent` - ビューア内でイベントが発生するたびに発生するトリガーです。Adobe Analyticsなど、イベントトラッキングシステムで処理される可能性があります。 コールバックハンドラーは次の引数を取ります。

   * `objID {String}` は現在使用されていません。
   * `compClass {String}` は現在使用されていません。
   * イベントをトリガーしたビューアのSDK コンポーネントのインスタンス名を `instName {String}` します。
   * イベ `timeStamp {Number}` トタイムスタンプ。
   * イベ `eventInfo {String}` トペイロード。

[VideoViewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) および [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926) も参照してください。
