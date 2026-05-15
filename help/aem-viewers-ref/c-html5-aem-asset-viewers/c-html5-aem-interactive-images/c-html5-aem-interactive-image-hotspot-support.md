---
title: Hotspot サポート
description: Hotspot サポート
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
TQID: 'https://experienceleague.adobe.com/kvYBwi70uYXIK8D6MeNgZN74h3X6jBfmOLj1SjlKEzs'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# Hotspot サポート{#hotspot-support}

ビューアは、メインビューの上にホットスポットアイコンをレンダリングすることをサポートしています。 ホットスポットアイコンの外観は、ホットスポット セクションで説明されているように、CSSによって制御されます。

[ ホットスポット ](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)を参照してください。

ホットスポットは、JavaScript コールバックをトリガーしてホスティング web ページのクイックビュー機能をアクティブにするか、ユーザーを外部web ページにリダイレクトできます。

## クイックビューホットスポット {#section-cda48fc9730142d0bb3326bac7df3271}

これらの種類のホットスポットは、Adobe Experience Manager Assets オンデマンドのDynamic Mediaの「クイックビュー」アクションタイプを使用して作成する必要があります。 ユーザーがそのようなホットスポットをアクティベートすると、ビューアは`quickViewActivate` JavaScript コールバックを実行し、ホットスポットデータをそのコールバックに渡します。 埋め込みweb ページがこのコールバックをリッスンすることが期待されます。 ページをトリガーすると、独自のクイックビュー実装が開きます。

## 外部web ページへのリダイレクト {#section-ef820c71251e4215800bb99c0c9ebe16}

Experience Manager AssetsのDynamic Mediaで「クイックビュー」というアクションタイプ用に作成されたホットスポット – オンデマンドでは、ユーザーを外部URLにリダイレクトします。 オーサリング中に行った設定に応じて、URLは新しいブラウザータブ、同じウィンドウ、または名前付きブラウザウィンドウで開きます。
