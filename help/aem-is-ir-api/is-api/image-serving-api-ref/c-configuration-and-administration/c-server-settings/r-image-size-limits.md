---
description: これらのサーバー設定を使用して、画像サイズの制限を設定します。
solution: Experience Manager
title: 画像サイズの制限
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 75ec58ee-8c98-46cb-96b2-79d1c32e576f
TQID: 'https://experienceleague.adobe.com/-xOEUXOC5tk9b9miYQWTmC73EsZbSo9Zzn8AedEksEI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 233
ht-degree: 0%

---

# 画像サイズの制限{#image-size-limits}

これらのサーバー設定を使用して、画像サイズの制限を設定します。

## IS::MaxMessageSize – 応答サイズの制限 {#section-bd942385d4d144cd904003695d72c85e}

Image Serverが[!DNL Platform Server]に送信できるデータのサイズを制限します。 これにより、Image ServingがHTTP （M バイト）経由でクライアントに返すことができるエンコード/圧縮された応答イメージのサイズが制限されます。

## IS::MaxRenderRgnPixels – 出力画像サイズの制限 {#section-868ceb9764dd42dfb133ffeb72f9d3fb}

Image Serverで生成できる画像のサイズを制限します（ファイルに保存される画像を除く）。 0を超える整数値（単位は百万ピクセル）。 レンダリング操作がサイズ制限を超える場合は、エラーが返されます。 デフォルトは16です。

## IS::MaxSavePixels - ファイルに保存するサイズ制限 {#section-d1547c4afa88467080ab08356f775e06}

Image Serverが`req=saveToFile` コマンドを使用してファイルに書き込む画像のサイズを制限します。 0を超える整数値（単位は百万ピクセル）。 ファイルの保存操作がその制限を超える場合は、エラーが返されます。 デフォルトは1億ピクセルです。

## IS::MaxNonDsfSize - PTIFF以外の入力画像のサイズ制限 {#section-50de28a7158a436393cce5da0d1e4d46}

Image Serverが開くことを許可されているPTIFF以外の画像の最大サイズ（Mpixels単位）。 画像サービングは、この制限を超えるPTIFF以外の画像にアクセスしようとしたときにエラーを返します。

>[!NOTE]
>
>この値を高く設定すると、Image Serverがメモリ不足になり、クラッシュなどのエラーが発生する可能性があります。
