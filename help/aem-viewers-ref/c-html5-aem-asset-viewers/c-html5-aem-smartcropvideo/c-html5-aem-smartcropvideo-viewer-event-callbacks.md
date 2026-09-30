---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 21962c01-f224-408d-8072-1c7f5d78ac4b
TQID: 'https://experienceleague.adobe.com/R1-8A1QXgy7TwEtZRMGt45D6WcM0AgqalP3wIbSCklU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%
---
# イベントコールバック{#event-callbacks}

ビューアは、Web ページがビューアの初期化プロセスまたはランタイム動作をトラッキングするために使用するJavaScript イベントコールバックをサポートしています。

コールバックハンドラーは、`handlers` プロパティを持つイベント名と対応するハンドラー関数をビューアのコンストラクターの`config` JSON オブジェクトに渡すことによって割り当てられます。 または、`setHandlers()` API メソッドを使用することもできます。

サポートされるビューアイベントには、次のものがあります。

* `initComplete` - ビューアの初期化が完了し、すべての内部コンポーネントが作成されたときにトリガーが発生します。これにより、`getComponent()` APIを使用できます。 コールバックハンドラーは引数を受け取りません。

* `trackEvent` - Adobe Analyticsなどのイベントトラッキングシステムで処理できるビューア内でイベントが発生するたびにトリガーします。 コールバックハンドラーは次の引数を取ります。

  * `objID {String}`は現在使用されていません。
  * `compClass {String}`は現在使用されていません。
  * `instName {String}` イベントをトリガーしたViewer SDK コンポーネントのインスタンス名。
  * `eventInfo {String}` イベントペイロード。

[SmartCropVideoViewerも参照してください]
（/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md）および[setHandlers](/help/aem-viewers-ref/c-html5-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-aem-smartcropvideo-viewer-javascriptapiref/r-html5-aem-smartcropvideo-viewer-javascriptapiref-sethandlers.md)。
