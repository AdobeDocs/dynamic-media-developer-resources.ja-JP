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

ビューアでは、メインビューの上部にあるホットスポットアイコンと画像マップ領域のレンダリングがサポートされています。 ホットスポットアイコンと領域の外観は、ホットスポットと画像マップのカスタマイズの節で説明されているように、CSS を通じて制御します。

詳しくは、 [ホットスポットと画像マップ](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74).

ホットスポットと地域は、JavaScript コールバックを呼び出すことで、ホストしている Web ページでクイックビュー機能を有効にするか、ユーザーを外部 Web ページにリダイレクトすることができます。

## クイックビューのホットスポット {#section-cda48fc9730142d0bb3326bac7df3271}

これらのタイプのホットスポットまたは画像マップは、Adobe Experience ManagerのDynamic Mediaの「クイックビュー」アクションタイプを使用してオーサリングする必要があります。 ユーザーがそのようなホットスポットまたは画像マップをアクティブにすると、ビューアは `quickViewActivate` JavaScript コールバックを呼び出し、ホットスポットまたは画像マップのデータをそれに渡します。 埋め込み Web ページがこのコールバックをリッスンする必要があります。 ページのトリガー時に、独自のクイックビュー実装が開きます。

## 外部 Web ページにリダイレクト {#section-ef820c71251e4215800bb99c0c9ebe16}

Experience ManagerのDynamic Mediaのアクションタイプ「クイックビュー」用に作成されたホットスポットまたは画像マップは、ユーザーを外部 URL にリダイレクトします。 オーサリング時におこなった設定に応じて、URL は新しいブラウザータブ、同じウィンドウ、または名前付きブラウザーウィンドウで開きます。
