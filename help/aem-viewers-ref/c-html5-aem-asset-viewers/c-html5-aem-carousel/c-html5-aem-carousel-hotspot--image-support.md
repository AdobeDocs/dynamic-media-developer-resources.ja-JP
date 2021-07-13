---
description: ホットスポットと画像マップのサポート
solution: Experience Manager
title: ホットスポットと画像マップのサポート
feature: Dynamic Media Classic，ビューア，SDK/API，カルーセルバナー
role: Developer,User
exl-id: b441e241-809e-47cf-a309-57283bd0532b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# ホットスポットと画像マップのサポート{#hotspot-and-image-maps-support}

ビューアでは、メインビューの上部にあるホットスポットアイコンと画像マップ領域のレンダリングがサポートされています。 ホットスポットのアイコンと領域の外観は、ホットスポットと画像マップのカスタマイズの節で説明されているように、CSSを通じて制御します。

[ホットスポットと画像マップ](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)を参照してください。

ホットスポットと地域は、JavaScriptコールバックを呼び出すことで、ホストしているWebページでクイックビュー機能を有効にするか、ユーザーを外部Webページにリダイレクトすることができます。

## クイックビューホットスポット {#section-cda48fc9730142d0bb3326bac7df3271}

AEMのDynamic Mediaの「クイックビュー」アクションタイプを使用して、これらのタイプのホットスポットまたは画像マップをオーサリングする必要があります。 ユーザーがそのようなホットスポットまたは画像マップをアクティブにすると、ビューアは`quickViewActivate` JavaScriptコールバックを実行し、ホットスポットまたは画像マップのデータを渡します。 埋め込みWebページは、このコールバックをリッスンする必要があります。 ページをトリガーすると、独自のクイックビュー実装が開きます。

## 外部Webページにリダイレクト {#section-ef820c71251e4215800bb99c0c9ebe16}

AEMのDynamic Mediaでアクションタイプ「クイックビュー」用に作成されたホットスポットまたは画像マップは、ユーザーを外部URLにリダイレクトします。 オーサリング時におこなった設定に応じて、URLは新しいブラウザータブ、同じウィンドウ、または指定されたブラウザーウィンドウで開きます。
