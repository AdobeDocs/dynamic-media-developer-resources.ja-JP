---
description: これらのサーバ設定を使用して、画像サイズの制限を設定します。
seo-description: これらのサーバ設定を使用して、画像サイズの制限を設定します。
seo-title: 画像サイズの制限
solution: Experience Manager
title: 画像サイズの制限
topic: Scene7 Image Serving - Image Rendering API
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 画像サイズの制限{#image-size-limits}

これらのサーバ設定を使用して、画像サイズの制限を設定します。

## IS::MaxMessageSize — 応答サイズの制限 {#section-bd942385d4d144cd904003695d72c85e}

Image Serverがプラットフォームサーバに送信できるデータのサイズを制限します。 これにより、HTTP（Mバイト）を使用して画像サービングからクライアントに返すことのできる、エンコードされた/圧縮された応答画像のサイズが制限されます。

## IS::MaxRenderRgnPixels — 出力画像サイズの制限 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Image Serverが生成できる画像のサイズを制限します（ファイルに保存された画像を除く）。 0より大きい整数値（百万ピクセル単位）。 レンダリング操作がサイズ制限を超える場合は、エラーが返されます。 初期設定は 16 です

## IS::MaxSavePixels — ファイルに保存する際のサイズ制限 {#section-d1547c4afa88467080ab08356f775e06}

Image Serverがコマンドを使用してファイルに書き込む画像のサイズを制限 `req=saveToFile` します。 0より大きい整数値（百万ピクセル単位）。 ファイルの保存操作がこの制限を超えると、エラーが返されます。 初期設定は1億ピクセルです。

## IS::MaxNonDsfSize - PTIFF以外の入力画像のサイズ制限 {#section-50de28a7158a436393cce5da0d1e4d46}

Image Serverで開くPTIFF以外の画像の最大サイズ（ピクセル単位）です。 この制限を超えるPTIFF以外の画像へのアクセスが試行されると、画像サービングからエラーが返されます。

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>この値を大きく設定すると、Image Serverのメモリ不足が発生し、クラッシュなどのエラーが発生する場合があります。

