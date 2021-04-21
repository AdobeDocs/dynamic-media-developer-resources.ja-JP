---
description: FlashアプリケーションのWebドメイン。 AdobeFlashアプリケーションでは、swf形式で配信される画像のプロパティにアクセスする必要がある場合があります。swfは、信頼するアプリケーションドメインの名前を登録することで、明示的にアクセスを許可する必要があります。
solution: Experience Manager
title: TrustedDomains *
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# TrustedDomains *{#trusteddomains}

FlashアプリケーションのWebドメイン。 AdobeFlashアプリケーションでは、swf形式で配信される画像のプロパティにアクセスする必要がある場合があります。swfは、信頼するアプリケーションドメインの名前を登録することで、明示的にアクセスを許可する必要があります。

## プロパティ {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Webドメイン名のカンマ区切りリストを含む文字列です。 空の場合、[!DNL swf]形式の応答内の画像のプロパティにアクセスするには、アプリケーションを画像レンダリングと同じドメインから提供する必要があります。

## 初期設定 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

存在しない場合は`default::TrustedDomains`から継承。

## 関連項目 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
