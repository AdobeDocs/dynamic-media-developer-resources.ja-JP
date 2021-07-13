---
description: FlashアプリケーションのWebドメイン。 AdobeFlashアプリケーションでは、swf形式で配信される画像のプロパティにアクセスする必要が生じる場合があります。swfは、信頼するアプリケーションドメインの名前を登録して、明示的にアクセス権を付与する必要があります。
solution: Experience Manager
title: TrustedDomains *
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# TrustedDomains *{#trusteddomains}

FlashアプリケーションのWebドメイン。 AdobeFlashアプリケーションでは、swf形式で配信される画像のプロパティにアクセスする必要が生じる場合があります。swfは、信頼するアプリケーションドメインの名前を登録して、明示的にアクセス権を付与する必要があります。

## プロパティ {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Webドメイン名のコンマ区切りリストを含む文字列。 空の場合、[!DNL swf]形式の応答の画像のプロパティにアクセスできるように、アプリケーションを画像レンダリングと同じドメインから提供する必要があります。

## 初期設定 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

存在しない場合は`default::TrustedDomains`から継承されます。

## 関連項目 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) ,  `mask=`,  [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
