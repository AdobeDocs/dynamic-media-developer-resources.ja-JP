---
description: インタラクティブビデオビューアは、設定パラメータとしてビューアに渡されるインタラクティブデータに基づくインタラクティブスウォッチのレンダリングをサポートします。
solution: Experience Manager
title: インタラクティブデータのサポート
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: 9118bf02-16ae-4dab-92e4-17347e866cc9
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 0%

---

# インタラクティブデータのサポート{#interactive-data-support}

インタラクティブビデオビューアは、設定パラメータとしてビューアに渡されるインタラクティブデータに基づくインタラクティブスウォッチのレンダリングをサポートします。

現在表示されているスウォッチは、関連付けられているビデオ時間領域に対応しています。 インタラクティブスウォッチをクリックまたはタップすると、作成者時にトリガーが割り当てます。

インタラクティブスウォッチは、JavaScript表示をトリガーしてホストするWebページのクイックコールバックをアクティブにするか、ユーザを外部Webページにリダイレクトすることができます。

## クイック表示について{#section-7990e44f641042d2a38ba20c9413b3f8}

これらのタイプのインタラクティブスウォッチは、オンデマンドで、アクションタイプ「quickview」を使用して作成する必要があります。 ユーザがこのようなスウォッチをアクティブにすると、ビューアは`quickViewActivate` JavaScriptコールバックを実行し、スウォッチデータを渡します。 埋め込み先のWebページは、このコールバックをリッスンし、トリガー時に、ページ独自のクイック表示実装を開く必要があります。

## 外部Webページにリダイレクト{#section-32ebe3c3a7f74892a428c5d48801de4d}

AEM Assetsでアクションタイプ「quickview」用に作成されたスウォッチ — オンデマンドで、ユーザを外部URLにリダイレクトします。 オーサリング時の設定に応じて、URLは新しいブラウザータブ、同じウィンドウ、または指定したブラウザーウィンドウで開くことができます。
