---
description: FlashアプリケーションのWebドメイン。 AdobeFlashアプリケーションでは、fmt=swfまたはfmt=swf3で配信される画像のプロパティにアクセスする必要が生じる場合があります。
solution: Experience Manager
title: TrustedDomains
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 925ac9d1-203c-4814-a701-71060bf47c20
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 3%

---

# TrustedDomains{#trusteddomains}

FlashアプリケーションのWebドメイン。 AdobeFlashアプリケーションでは、fmt=swfまたはfmt=swf3で配信される画像のプロパティにアクセスする必要が生じる場合があります。

swfは、信頼するアプリケーションドメインの名前を登録することで、明示的にアクセス権を付与する必要があります。

## プロパティ {#section-e7f95bbb749f441e83e90c2bc3d5a6e0}

Webドメイン名のコンマ区切りリストを含む文字列。 空の場合、swf形式の応答の画像のプロパティにアクセスできるように、アプリケーションは画像レンダリングと同じドメインから提供される必要があります。

## 初期設定 {#section-5c52ed3c7310488380f5a6f9540bf981}

存在しない場合は`default::TrustedDomains`から継承されます。

## 関連項目 {#section-65d0846e41674882a4d0d56a8f6d524b}

[fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
