---
description: これらのサーバ設定を使用して、画像サイズの制限を設定します。
solution: Experience Manager
title: 画像サイズの制限
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# 画像サイズの制限{#image-size-limits}

これらのサーバ設定を使用して、画像サイズの制限を設定します。

## IS::MaxMessageSize — 応答サイズの制限 {#section-bd942385d4d144cd904003695d72c85e}

Image Server がに送信できるデータのサイズを制限 [!DNL Platform Server]. これにより、画像サービングが HTTP（M バイト）を介してクライアントに返すことができる、エンコードされた/圧縮された応答画像のサイズが制限されます。

## IS::MaxRenderRgnPixels — 出力画像サイズの制限 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Image Server で生成できる画像のサイズを制限します（ファイルに保存された画像を除く）。 0 より大きい整数値（100 万ピクセル単位） レンダリング操作がサイズ制限を超える場合は、エラーが返されます。 初期設定は 16 です

## IS::MaxSavePixels — ファイルに保存する際のサイズ制限 {#section-d1547c4afa88467080ab08356f775e06}

Image Server が書き込む画像のサイズを、 `req=saveToFile` コマンドを使用します。 0 より大きい整数値（100 万ピクセル単位） ファイルの保存操作がこの制限を超えると、エラーが返されます。 初期設定は 1 億ピクセルです。

## IS::MaxNonDsfSize - PTIFF 以外の入力画像のサイズ制限 {#section-50de28a7158a436393cce5da0d1e4d46}

Image Server で開くことができる PTIFF 以外の画像の最大サイズ（ピクセル単位）です。 この制限を超える PTIFF 以外の画像にアクセスしようとすると、画像サービングはエラーを返します。

>[!NOTE]
>
>この値を大きく設定すると、Image Server のメモリが不足し、クラッシュを含むエラーが発生する場合があります。
