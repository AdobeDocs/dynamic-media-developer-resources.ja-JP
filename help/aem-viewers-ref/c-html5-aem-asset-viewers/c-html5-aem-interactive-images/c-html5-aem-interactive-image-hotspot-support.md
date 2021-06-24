---
description: ホットスポットのサポート
solution: Experience Manager
title: ホットスポットのサポート
feature: Dynamic Media Classic，ビューア，SDK/API，インタラクティブ画像
role: Developer,Business Practitioner
exl-id: 9b9ccdf4-4639-4ba8-988c-c68d81192619
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# ホットスポットのサポート{#hotspot-support}

ビューアでは、メインビューの上部にあるホットスポットアイコンのレンダリングがサポートされています。 ホットスポットアイコンの外観は、ホットスポットの節で説明しているようにCSSで制御します。

[ホットスポット](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)を参照してください。

ホットスポットは、JavaScriptコールバックを呼び出すことで、ホストしているWebページでクイックビュー機能を有効にするか、ユーザーを外部Webページにリダイレクトすることができます。

## クイックビューホットスポット {#section-cda48fc9730142d0bb3326bac7df3271}

これらのタイプのホットスポットは、Dynamic Media、AEM Assets - On Demandの「クイックビュー」アクションタイプを使用してオーサリングする必要があります。 ユーザーがこのようなホットスポットをアクティブ化すると、ビューアは`quickViewActivate` JavaScriptコールバックを実行し、ホットスポットデータをそのホットスポットに渡します。 埋め込みWebページは、このコールバックをリッスンする必要があります。 ページをトリガーすると、独自のクイックビュー実装が開きます。

## 外部Webページにリダイレクト {#section-ef820c71251e4215800bb99c0c9ebe16}

AEM AssetsのDynamic Mediaでアクションタイプ「クイックビュー」用に作成されたホットスポットは、オンデマンドでユーザーを外部URLにリダイレクトします。 オーサリング時におこなった設定に応じて、URLは新しいブラウザータブ、同じウィンドウ、または指定されたブラウザーウィンドウで開きます。
