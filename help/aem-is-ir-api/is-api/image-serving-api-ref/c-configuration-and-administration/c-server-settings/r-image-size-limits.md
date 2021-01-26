---
description: 画像サイズの制限を設定するには、次のサーバー設定を使用します。
seo-description: 画像サイズの制限を設定するには、次のサーバー設定を使用します。
seo-title: 画像サイズの制限
solution: Experience Manager
title: 画像サイズの制限
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6736e652-c495-45a2-bdd2-9975f99af0a2
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---


# 画像サイズの制限{#image-size-limits}

画像サイズの制限を設定するには、次のサーバー設定を使用します。

## IS::MaxMessageSize — 応答サイズの制限{#section-bd942385d4d144cd904003695d72c85e}

Image Serverがプラットフォームサーバに送信できるデータのサイズを制限します。 これにより、画像サービングがHTTP（Mバイト）を使用してクライアントに返すことのできる、エンコード/圧縮された応答画像のサイズが制限されます。

## IS::MaxRenderRgnPixels — 出力画像サイズの制限{#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Image Serverが生成できる画像のサイズを制限します（ファイルに保存した画像を除く）。 0（ピクセル単位）より大きい整数値。 レンダリング操作がサイズ制限を超える場合は、エラーが返されます。 初期設定は 16 です

## IS::MaxSavePixels — ファイルに保存するサイズの制限{#section-d1547c4afa88467080ab08356f775e06}

`req=saveToFile`コマンドを使用して、Image Serverがファイルに書き込む画像のサイズを制限します。 0（ピクセル単位）より大きい整数値。 ファイルの保存操作がその制限を超える場合は、エラーが返されます。 初期設定は1億ピクセルです。

## IS::MaxNonDsfSize - PTIFF以外の入力画像のサイズ制限{#section-50de28a7158a436393cce5da0d1e4d46}

Image Serverで開くPTIFF以外の画像の最大サイズ（ピクセル単位）です。 この制限を超える非PTIFF画像へのアクセスが試行された場合、画像サービングはエラーを返します。

>[!NOTE]
>
>この値を大きく設定すると、Image Serverのメモリ不足が発生し、クラッシュなどのエラーが発生する場合があります。

