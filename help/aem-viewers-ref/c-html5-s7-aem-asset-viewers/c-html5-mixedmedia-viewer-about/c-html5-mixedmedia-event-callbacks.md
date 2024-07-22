---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1a7b51c1-baa7-4ae3-b6b7-17478055a605
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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
   * イベントをトリガーしたビューア SDK コンポーネントのインスタンス名を `instName {String}` します。
   * イベ `timeStamp {Number}` トタイムスタンプ。
   * イベ `eventInfo {String}` トペイロード。

[MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195) および [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3) も参照してください。
