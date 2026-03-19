---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 21962c01-f224-408d-8072-1c7f5d78ac4b
source-git-commit: 07380e01e4eed6a65ba8821eee3db6fd9bb19639
workflow-type: tm+mt
source-wordcount: '150'
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
   * イベ `eventInfo {String}` トペイロード。

[SmartCropVideoViewer] も参照してください
（/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md）と [setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md)。
