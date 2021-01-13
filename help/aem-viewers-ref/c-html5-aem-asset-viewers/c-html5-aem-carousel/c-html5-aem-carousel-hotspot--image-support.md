---
description: ホットスポットと画像マップのサポート
solution: Experience Manager
title: ホットスポットと画像マップのサポート
topic: Dynamic media
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---


# ホットスポットと画像マップのサポート{#hotspot-and-image-maps-support}

ビューアでは、メイン表示の上部にあるホットスポットアイコンと画像マップ領域のレンダリングがサポートされています。 ホットスポットアイコンと領域の外観は、「ホットスポットと画像マップのカスタマイズ」の項で説明されているように、CSSを使用して制御します。

[ホットスポットと画像マップ](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)を参照してください。

ホットスポットと地域は、JavaScriptコールバックをトリガーしてホストするWebページのクイック表示機能をアクティブにするか、ユーザーを外部Webページにリダイレクトすることができます。

## クイック表示ホットスポット{#section-cda48fc9730142d0bb3326bac7df3271}

この種類のホットスポットまたは画像マップは、AEMのDynamic Mediaで、「クイック表示」アクションタイプを使用して作成する必要があります。 ユーザがそのようなホットスポットや画像マップをアクティブにすると、ビューアは`quickViewActivate` JavaScriptコールバックを実行し、ホットスポットや画像マップデータを渡します。 埋め込み先のWebページは、このコールバックをリッスンする必要があります。 ページをトリガーすると、独自のクイック表示実装が開きます。

## 外部Webページにリダイレクト{#section-ef820c71251e4215800bb99c0c9ebe16}

AEMのDynamic Mediaで、アクションタイプ「クイック表示」用に作成されたホットスポットまたは画像マップは、ユーザーを外部URLにリダイレクトします。 オーサリング中に行われた設定に応じて、URLが新しいブラウザータブ、同じウィンドウ、または指定したブラウザーウィンドウに開きます。
