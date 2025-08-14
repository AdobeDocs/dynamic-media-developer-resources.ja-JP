---
title: ホットスポットと画像マップのサポート
description: ホットスポットと画像マップのサポート
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 8d5dbc2d2b5e228f8496fd71633bf1cb96218226
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# ホットスポットと画像マップのサポート{#hotspot-and-image-maps-support}

ビューアは、メインビューの上部にあるホットスポットアイコンと画像マップ領域のレンダリングをサポートしています。 ホットスポットのアイコンと領域の外観は、ホットスポットと画像マップのカスタマイズの節で説明しているように、CSS で制御されます。

[ ホットスポットと画像マップ ](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74) を参照してください。

ホットスポットとリージョンは、JavaScript コールバックをトリガーしてホスティング web ページ上でクイックビュー機能をアクティブ化するか、ユーザーを外部 web ページにリダイレクトできます。

## クイックビューホットスポット {#section-cda48fc9730142d0bb3326bac7df3271}

このようなホットスポットや画像マップは、Adobe Experience Managerの Dynamic Media の「クイックビュー」アクションタイプを使用して作成する必要があります。 ユーザーがそのようなホットスポットまたは画像マップをアクティブ化すると、ビューアは `quickViewActivate` JavaScript コールバックを実行し、ホットスポットまたは画像マップのデータをそれに渡します。 埋め込まれる web ページは、このコールバックをリッスンすることが想定されます。 ページをトリガーすると、独自のクイックビュー実装が開きます。

## 外部 Web ページにリダイレクト {#section-ef820c71251e4215800bb99c0c9ebe16}

Experience Managerの Dynamic Media のアクションタイプ「クイックビュー」用に作成されたホットスポットまたは画像マップは、外部 URL にユーザーをリダイレクトします。 オーサリング時に行った設定に応じて、URL は新しいブラウザータブ、同じウィンドウ、または名前付きブラウザウィンドウで開きます。
