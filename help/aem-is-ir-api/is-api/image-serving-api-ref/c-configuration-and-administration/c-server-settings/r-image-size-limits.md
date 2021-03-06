---
description: これらのサーバー設定を使用して、画像サイズの制限を設定します。
solution: Experience Manager
title: 画像サイズの制限
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 0%

---

# 画像サイズの制限{#image-size-limits}

これらのサーバー設定を使用して、画像サイズの制限を設定します。

## IS::MaxMessageSize — 応答サイズの制限 {#section-bd942385d4d144cd904003695d72c85e}

Image ServerがPlatform Serverに送信できるデータのサイズを制限します。 これにより、画像サービングがHTTP（Mバイト）を介してクライアントに返すことができる、エンコード/圧縮された応答画像のサイズが効果的に制限されます。

## IS::MaxRenderRgnPixels — 出力画像サイズの制限 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Image Serverで生成できる画像のサイズを制限します（ファイルに保存する画像を除く）。 0より大きい整数値（百万ピクセル単位）。 レンダリング操作がサイズ制限を超える場合、エラーが返されます。 初期設定は 16 です

## IS::MaxSavePixels — ファイルに保存する際のサイズ制限 {#section-d1547c4afa88467080ab08356f775e06}

`req=saveToFile`コマンドを使用して、Image Serverがファイルに書き込む画像のサイズを制限します。 0より大きい整数値（百万ピクセル単位）。 ファイルの保存操作がその制限を超えると、エラーが返されます。 初期設定は1億ピクセルです。

## IS::MaxNonDsfSize — 非PTIFF入力画像のサイズ制限 {#section-50de28a7158a436393cce5da0d1e4d46}

Image Serverで開くことが許可されるPTIFF以外の画像の最大サイズ（ピクセル単位）です。 この制限を超えるPTIFF以外の画像にアクセスしようとすると、画像サービングはエラーを返します。

>[!NOTE]
>
>この値を大きく設定すると、Image Serverのメモリが不足し、クラッシュを含むエラーが発生する場合があります。
