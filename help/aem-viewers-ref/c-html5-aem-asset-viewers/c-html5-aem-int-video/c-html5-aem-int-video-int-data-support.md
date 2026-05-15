---
title: インタラクティブなデータ処理
description: インタラクティブビデオビューアは、設定パラメーターとしてビューアに渡されるインタラクティブデータに基づくインタラクティブスウォッチのレンダリングをサポートしています。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
TQID: 'https://experienceleague.adobe.com/HE4LeluT9FWi8xgQf259b1yakK0oQjeR3rDME0juZiU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 223
ht-degree: 0%

---

# インタラクティブなデータ処理{#interactive-data-support}

インタラクティブビデオビューアは、設定パラメーターとしてビューアに渡されるインタラクティブデータに基づくインタラクティブスウォッチのレンダリングをサポートしています。

現在表示されているスウォッチは、関連付けられているビデオ時間領域に対応します。 インタラクティブなスウォッチトリガーをクリックまたはタップすると、作成時に割り当てられたアクションが表示されます。

インタラクティブスウォッチは、JavaScript コールバックをトリガーしてホスティング web ページでクイックビューをアクティブ化するか、ユーザーを外部web ページにリダイレクトできます。

## クイックビューについて {#section-7990e44f641042d2a38ba20c9413b3f8}

これらのインタラクティブスウォッチは、Adobe Experience Manager Assets オンデマンドのアクションタイプ「クイックビュー」を使用して作成する必要があります。 ユーザーがそのようなスウォッチをアクティベートすると、ビューアは`quickViewActivate` JavaScript コールバックを実行し、スウォッチデータをそのスウォッチに渡します。 埋め込みweb ページがこのコールバックをリッスンし、トリガーすると、ページが独自のクイックビュー実装を開くことが期待されます。

## 外部web ページへのリダイレクト {#section-32ebe3c3a7f74892a428c5d48801de4d}

Experience Manager Assetsのアクションタイプ「クイックビュー」用に作成されたスウォッチ – オンデマンドでユーザーを外部URLにリダイレクトします。 オーサリング時の設定に応じて、URLは新しいブラウザータブ、同じウィンドウ、または名前付きブラウザウィンドウのいずれかで開くことができます。
