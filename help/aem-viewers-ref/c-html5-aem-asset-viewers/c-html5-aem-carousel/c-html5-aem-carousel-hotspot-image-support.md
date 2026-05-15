---
title: ホットスポットと画像マップのサポート
description: ホットスポットと画像マップのサポート
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
TQID: 'https://experienceleague.adobe.com/lXiW-xoAeHFZic9fH-AN491yZfrPE1R0S53FBS1oMig'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 212
ht-degree: 0%

---

# ホットスポットと画像マップのサポート{#hotspot-and-image-maps-support}

ビューアは、メインビューの上にホットスポットアイコンと画像マップ領域のレンダリングをサポートしています。 ホットスポットのアイコンと領域の外観は、ホットスポットと画像マップのカスタマイズの節で説明されているように、CSSを使用して制御されます。

[ ホットスポットと画像マップ ](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)を参照してください。

ホットスポットとリージョンは、JavaScript コールバックをトリガーしてホスティング web ページのクイックビュー機能をアクティブにするか、ユーザーを外部web ページにリダイレクトできます。

## クイックビューホットスポット {#section-cda48fc9730142d0bb3326bac7df3271}

これらの種類のホットスポットまたは画像マップは、Adobe Experience ManagerのDynamic Mediaの「クイックビュー」アクションタイプを使用して作成する必要があります。 ユーザーがそのようなホットスポットまたは画像マップをアクティブ化すると、ビューアは`quickViewActivate` JavaScript コールバックを実行し、ホットスポットまたは画像マップデータをそれに渡します。 埋め込みweb ページがこのコールバックをリッスンすることが期待されます。 ページをトリガーすると、独自のクイックビュー実装が開きます。

## 外部web ページへのリダイレクト {#section-ef820c71251e4215800bb99c0c9ebe16}

Experience ManagerのDynamic Mediaで「クイックビュー」というアクションタイプ用に作成されたホットスポットまたは画像マップは、ユーザーを外部URLにリダイレクトします。 オーサリング中に行った設定に応じて、URLは新しいブラウザータブ、同じウィンドウ、または名前付きブラウザウィンドウで開きます。
