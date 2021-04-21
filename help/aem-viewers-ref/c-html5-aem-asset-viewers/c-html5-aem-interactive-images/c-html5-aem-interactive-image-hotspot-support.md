---
description: ホットスポットのサポート
solution: Experience Manager
title: ホットスポットのサポート
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,Business Practitioner
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# ホットスポットのサポート{#hotspot-support}

ビューアでは、メイン表示の上部にあるホットスポットアイコンのレンダリングがサポートされています。 ホットスポットアイコンの外観は、「ホットスポット」の項で説明されているように、CSSを使用して制御します。

[ホットスポット](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)を参照してください。

ホットスポットは、JavaScript表示をトリガーしてホストWebページのクイックコールバック機能をアクティブにするか、ユーザーを外部Webページにリダイレクトすることができます。

## クイック表示ホットスポット{#section-cda48fc9730142d0bb3326bac7df3271}

この種のホットスポットは、AEM AssetsのDynamic Mediaにある「クイック表示」アクションタイプを使用してオンデマンドで作成する必要があります。 ユーザーがこのようなホットスポットをアクティブにすると、ビューアは`quickViewActivate` JavaScriptコールバックを実行し、ホットスポットデータを渡します。 埋め込み先のWebページは、このコールバックをリッスンする必要があります。 ページをトリガーすると、独自のクイック表示実装が開きます。

## 外部Webページにリダイレクト{#section-ef820c71251e4215800bb99c0c9ebe16}

AEM AssetsのDynamic Mediaで、アクションタイプ「クイック表示」用に作成されたホットスポット — オンデマンドで、ユーザーを外部URLにリダイレクトします。 オーサリング中に行われた設定に応じて、URLが新しいブラウザータブ、同じウィンドウ、または指定したブラウザーウィンドウに開きます。
