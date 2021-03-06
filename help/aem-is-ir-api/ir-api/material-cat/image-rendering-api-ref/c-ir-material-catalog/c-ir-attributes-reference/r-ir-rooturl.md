---
description: 相対画像URLのルートURL。 相対画像URLのルートURLを指定します。 src=値が{中括弧}で囲まれている場合、attribute RootUrlが属性RootPathの代わりに使用されます。
solution: Experience Manager
title: RootUrl *
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 3%

---

# RootUrl *{#rooturl}

相対画像URLのルートURL。 相対画像URLのルートURLを指定します。 src=値が{中括弧}で囲まれている場合、attribute::RootUrlがattribute::RootPathの代わりに使用されます。

## プロパティ {#section-69cd0f71ea614770a8778c745d23197a}

テキスト文字列の値。 先頭のプロトコル識別子を含む、絶対URLルートパス。 次のプロトコルがサポートされています。HTTP、HTTPS、FTP。

## 初期設定 {#section-7a81569728474725a70f3a2cc4d48e85}

定義されていない場合は`default::RootUrl`から継承されます。 定義されているが空の場合、相対URLはこのマテリアルカタログではサポートされません。

## 関連項目 {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [attribute:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
