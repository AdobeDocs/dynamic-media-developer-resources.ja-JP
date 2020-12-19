---
description: FlashアプリケーションのWebドメイン。 AdobeFlashアプリケーションでは、fmt=swfまたはfmt=swf3と共に配信される画像のプロパティへのアクセスが必要になる場合があります。
seo-description: FlashアプリケーションのWebドメイン。 AdobeFlashアプリケーションでは、fmt=swfまたはfmt=swf3と共に配信される画像のプロパティへのアクセスが必要になる場合があります。
seo-title: TrustedDomains
solution: Experience Manager
title: TrustedDomains
topic: Scene7 Image Serving - Image Rendering API
uuid: 1d056d68-b699-413c-897c-8612444735c5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# TrustedDomains{#trusteddomains}

FlashアプリケーションのWebドメイン。 AdobeFlashアプリケーションでは、fmt=swfまたはfmt=swf3と共に配信される画像のプロパティへのアクセスが必要になる場合があります。

swfは、信頼するアプリケーションドメインの名前を登録することで、明示的にアクセスを許可する必要があります。

## プロパティ {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Webドメイン名のカンマ区切りリストを含む文字列です。 空の場合、swf形式の応答で画像のプロパティにアクセスするには、画像レンダリングと同じドメインからアプリケーションを提供する必要があります。

## 初期設定 {#section-5c52ed3c7310488380f5a6f9540bf981}

存在しない場合は`default::TrustedDomains`から継承。

## 関連項目 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
