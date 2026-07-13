---
title: RootURL
description: 相対画像URLのルート URL。 相対画像URLのルート URLを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
TQID: 'https://experienceleague.adobe.com/1wKgvbd1t4HyDlz-CTDkp2gQuryBJYfMyDG7SmVgNwE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 86
ht-degree: 3%

---

# RootURL{#rooturl}

相対画像URLのルート URL。 相対画像URLのルート URLを指定します。 `src=`の値が{curly braces}で囲まれている場合、`attribute::RootPath`の代わりに`attribute::RootUrl`が使用されます。

## プロパティ {#section-69cd0f71ea614770a8778c745d23197a}

テキスト文字列値。 プロトコル識別子の先頭を含む絶対URL ルートパス。 HTTP、HTTPS、FTPのプロトコルがサポートされています。

## 初期設定 {#section-7a81569728474725a70f3a2cc4d48e85}

定義されていない場合、`default::RootUrl`から継承されます。 定義されていても空の場合、相対URLはこのマテリアルカタログではサポートされていません。

## 関連項目 {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)、`mask=`、[属性:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)

