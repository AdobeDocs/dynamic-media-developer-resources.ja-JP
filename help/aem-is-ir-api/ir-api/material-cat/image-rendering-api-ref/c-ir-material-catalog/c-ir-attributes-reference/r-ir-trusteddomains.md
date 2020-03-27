---
description: FlashアプリケーションのWebドメイン。 Adobe Flashアプリケーションでは、swf形式で配信される画像のプロパティへのアクセスが必要な場合があります。swfは、信頼するアプリケーションドメインの名前を登録することで、明示的にアクセスを許可する必要があります。
seo-description: FlashアプリケーションのWebドメイン。 Adobe Flashアプリケーションでは、swf形式で配信される画像のプロパティへのアクセスが必要な場合があります。swfは、信頼するアプリケーションドメインの名前を登録することで、明示的にアクセスを許可する必要があります。
seo-title: TrustedDomains *
solution: Experience Manager
title: TrustedDomains *
topic: Scene7 Image Serving - Image Rendering API
uuid: c50180b1-9af7-45f1-878f-59f41f9958ae
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# TrustedDomains *{#trusteddomains}

FlashアプリケーションのWebドメイン。 Adobe Flashアプリケーションでは、swf形式で配信される画像のプロパティへのアクセスが必要な場合があります。swfは、信頼するアプリケーションドメインの名前を登録することで、明示的にアクセスを許可する必要があります。

## プロパティ {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Webドメイン名のコンマ区切りリストを含む文字列。 空の場合、形式設定された応答で画像のプロパティにアクセスできるように、アプリケーションは画像レンダリングと同じドメインから供給される [!DNL swf]必要があります。

## 初期設定 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

存在しない場 `default::TrustedDomains` 合に継承されます。

## 関連項目 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272) , `mask=`, [attribute::RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)
