---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 7bd2e167-d04c-43e2-a71c-e2b3dddb13a0
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
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
   * `eventInfo {String}` イベントペイロード

[eCatalogViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-ecatalogviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) および [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856) も参照してください。
