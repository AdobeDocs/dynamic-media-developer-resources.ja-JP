---
title: ホットスポットのサポート
description: ホットスポットのサポート
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 0%

---

# ホットスポットのサポート{#hotspot-support}

ビューアでは、メインビューの上部にあるホットスポットアイコンのレンダリングがサポートされています。 ホットスポットアイコンの外観は、ホットスポットの節で説明しているように CSS で制御します。

[ ホットスポット ](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74) を参照してください。

ホットスポットは、JavaScript コールバックを呼び出すことで、ホストしている Web ページでクイックビュー機能を有効にするか、ユーザーを外部 Web ページにリダイレクトすることができます。

## クイックビューホットスポット {#section-cda48fc9730142d0bb3326bac7df3271}

これらのタイプのホットスポットは、Adobe Experience Manager Assets - On-demand の、Dynamic Mediaの「クイックビュー」アクションタイプを使用してオーサリングする必要があります。 ユーザーがこのようなホットスポットをアクティブにすると、ビューアは `quickViewActivate` JavaScript コールバックを実行し、ホットスポットデータを渡します。 埋め込み Web ページは、このコールバックをリッスンする必要があります。 ページをトリガーすると、独自のクイックビュー実装が開きます。

## 外部 Web ページにリダイレクト {#section-ef820c71251e4215800bb99c0c9ebe16}

Experience ManagerアセットのDynamic Mediaでアクションタイプ「クイックビュー」用に作成されたホットスポット — オンデマンドは、ユーザーを外部 URL にリダイレクトします。 オーサリング中におこなった設定に応じて、URL は新しいブラウザータブ、同じウィンドウ、または名前付きブラウザーウィンドウで開きます。
