---
description: Flashアプリケーションの web ドメイン。 AdobeFlashアプリケーションでは、fmt=swf または fmt=swf3 で配信される画像のプロパティにアクセスする必要がある場合があります。
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 2%

---

# TrustedDomains{#trusteddomains}

Flashアプリケーションの web ドメイン。 AdobeFlashアプリケーションでは、fmt=swf または fmt=swf3 で配信される画像のプロパティにアクセスする必要がある場合があります。

swf は、信頼するアプリケーションドメインの名前を登録して、明示的にアクセスを許可する必要があります。

## プロパティ {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Web ドメイン名のコンマ区切りリストを含む文字列。 空の場合、swf 形式の応答で画像のプロパティにアクセスできるようにするには、画像レンダリングと同じドメインからアプリケーションを提供する必要があります。

## 初期設定 {#section-5c52ed3c7310488380f5a6f9540bf981}

存在しない場合は、`default::TrustedDomains` から継承されます。

## 関連項目 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
