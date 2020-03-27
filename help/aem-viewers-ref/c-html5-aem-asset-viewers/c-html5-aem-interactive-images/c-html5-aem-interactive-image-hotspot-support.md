---
description: 'null'
seo-description: 'null'
seo-title: ホットスポットのサポート
solution: Experience Manager
title: ホットスポットのサポート
topic: Dynamic media
uuid: 62e0e55a-55a3-417d-ad51-ec77a7c16ac3
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ホットスポットのサポート{#hotspot-support}

ビューアでは、メインビューの上部でホットスポットアイコンのレンダリングがサポートされています。 ホットスポットアイコンの外観は、「ホットスポット」の節で説明されているように、CSSで制御します。

ホットスポッ [トを参照し](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/r-html5-aem-int-image-customize-hotspots.md#reference-2ac3cc414ef2467390bf53145f1d8d74)。

ホットスポットは、JavaScriptコールバックをトリガーしてホストするWebページ上のクイックビュー機能をアクティブにするか、ユーザーを外部Webページにリダイレクトすることができます。

## クイックビューのホットスポット {#section-cda48fc9730142d0bb3326bac7df3271}

これらのタイプのホットスポットは、ダイナミックメディアの「クイックビュー」アクションタイプ(AEM Assets - On Demand)を使用して作成する必要があります。 ユーザーがこのようなホットスポットをアクティブにすると、ビューアは `quickViewActivate` JavaScriptコールバックを実行し、ホットスポットデータを渡します。 埋め込みのWebページは、このコールバックをリッスンする必要があります。 ページがトリガーされると、独自のクイックビュー実装が開きます。

## 外部Webページにリダイレクト {#section-ef820c71251e4215800bb99c0c9ebe16}

AEM Assetsのダイナミックメディアでアクションタイプ「クイックビュー」用に作成されたホットスポット — オンデマンドで、ユーザーを外部URLにリダイレクトします。 オーサリング時に行った設定に応じて、URLは新しいブラウザータブ、同じウィンドウ、または指定したブラウザーウィンドウで開きます。
