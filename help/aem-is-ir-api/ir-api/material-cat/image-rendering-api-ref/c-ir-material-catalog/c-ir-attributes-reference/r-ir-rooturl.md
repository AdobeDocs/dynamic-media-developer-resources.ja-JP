---
title: RootUrl
description: 相対画像 URL のルート URL。 相対画像 URL のルート URL を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 094b5143-d4f0-412f-92cf-3522157cbeca
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 3%

---

# RootUrl{#rooturl}

相対画像 URL のルート URL。 相対画像 URL のルート URL を指定します。 `src=` 値が { 中括弧 } で囲まれている場合、`attribute::RootPath` の代わりに `attribute::RootUrl` が使用されます。

## プロパティ {#section-69cd0f71ea614770a8778c745d23197a}

テキスト文字列値。 先頭のプロトコル識別子を含む、URL ルートパスの絶対パス。 HTTP、HTTPS、FTP の各プロトコルがサポートされています。

## 初期設定 {#section-7a81569728474725a70f3a2cc4d48e85}

定義されていない場合は `default::RootUrl` から継承します。 定義されているが空の場合、このマテリアル カタログでは相対 URL はサポートされません。

## 関連項目 {#section-e33bbe7034b24367b68f9142718a8be1}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute:RootPath](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rootpath.md#reference-a4d7c96b62e14fcbad1740c702f160f3)
