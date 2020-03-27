---
description: 'null'
seo-description: 'null'
seo-title: ホットスポットと画像マップのサポート
solution: Experience Manager
title: ホットスポットと画像マップのサポート
topic: Dynamic media
uuid: 839b6a7f-4f6f-43ad-8eb8-254959c7fbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ホットスポットと画像マップのサポート{#hotspot-and-image-maps-support}

ビューアでは、メインビューの上部にあるホットスポットアイコンと画像マップ領域のレンダリングがサポートされています。 ホットスポットのアイコンと領域の外観は、「ホットスポットと画像マップのカスタマイズ」の説明に従ってCSSで制御します。

詳しくは、ホ [ットスポットと画像マップを参照してくださ](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/r-html5-aem-carousel-customize-hotspots-imagemaps.md#reference-2ac3cc414ef2467390bf53145f1d8d74)い。

ホットスポットと地域は、JavaScriptコールバックをトリガーして、ホストするWebページ上のクイックビュー機能をアクティブにするか、外部Webページにユーザーをリダイレクトすることができます。

## クイックビューのホットスポット {#section-cda48fc9730142d0bb3326bac7df3271}

これらのタイプのホットスポットまたは画像マップは、AEMのダイナミックメディアの「クイックビュー」アクションタイプを使用して作成する必要があります。 ユーザがこのようなホットスポットや画像マップをアクティブにすると、ビューアは `quickViewActivate` JavaScriptコールバックを実行し、ホットスポットや画像マップのデータを渡します。 埋め込みのWebページは、このコールバックをリッスンする必要があります。 ページがトリガーされると、独自のクイックビュー実装が開きます。

## 外部Webページにリダイレクト {#section-ef820c71251e4215800bb99c0c9ebe16}

AEMのダイナミックメディアでアクションタイプ「クイックビュー」用に作成されたホットスポットまたは画像マップは、ユーザーを外部URLにリダイレクトします。 オーサリング時に行った設定に応じて、URLは新しいブラウザータブ、同じウィンドウ、または指定したブラウザーウィンドウで開きます。
