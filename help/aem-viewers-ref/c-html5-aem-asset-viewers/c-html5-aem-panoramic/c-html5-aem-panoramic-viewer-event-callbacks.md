---
title: イベントコールバック
description: イベントコールバック
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: 24ea35c0-a0b1-4768-9336-94eb5e2d4fb2
source-git-commit: 8aebcacd5abdc23565aab1bc3506c36f055b6439
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---

# イベントコールバック{#event-callbacks}

ビューアでは、Web ページでビューアの初期化処理または実行時の動作の追跡に使用される JavaScript イベントコールバックがサポートされています。

コールバックハンドラーは、イベント名と対応するハンドラー関数を `handlers` プロパティを `config` ビューアのコンストラクター内の JSON オブジェクト。 または、 `setHandlers()` API メソッド。

サポートされるビューアイベントには、次のものがあります。

* `initComplete`  — ビューアの初期化が完了し、すべての内部コンポーネントが作成されたときにトリガーが発生し、 `getComponent()` API コールバックハンドラーは引数を取りません。
* `trackEvent` - Adobe Analyticsなどのイベントトラッキングシステムで処理できるビューア内でイベントが発生するたびにトリガーされます。 コールバックハンドラーは次の引数を取ります。

   * `objID {String}` 現在は使用されていません。
   * `compClass {String}` 現在は使用されていません。
   * `instName {String}` イベントをトリガーしたHTML5 ビューア SDK コンポーネントのインスタンス名。
   * `timeStamp {Number}` イベントのタイムスタンプ。
   * `eventInfo {String}` イベントペイロード。

