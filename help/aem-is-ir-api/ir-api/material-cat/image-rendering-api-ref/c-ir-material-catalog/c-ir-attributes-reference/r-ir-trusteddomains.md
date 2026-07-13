---
title: TrustedDomains
description: Flash アプリケーション web ドメイン。 Adobe Flash アプリケーションでは、swf形式で配信される画像のプロパティにアクセスする必要がある場合があります。 swfは、信頼するアプリケーションドメインの名前を登録することで、アクセスを明示的に許可する必要があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 41794f62-6140-4e54-9de2-908b20c51b37
TQID: 'https://experienceleague.adobe.com/GgLL3XL2Km0RvlfK3fjeD95FkgzO9OEcxNyyTZ8Y738'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 2%

---

# TrustedDomains{#trusteddomains}

Flash アプリケーション web ドメイン。 Adobe Flash アプリケーションでは、swf形式で配信される画像のプロパティにアクセスする必要がある場合があります。 swfは、信頼するアプリケーションドメインの名前を登録することで、アクセスを明示的に許可する必要があります。

## プロパティ {#section-5d6ecfa431a04abd8628a28e0ab3be83}

Web ドメイン名のコンマ区切りリストを含む文字列。 空の場合、[!DNL swf]形式の応答で画像のプロパティにアクセスするには、アプリケーションを画像レンダリングと同じドメインから提供する必要があります。

## 初期設定 {#section-8fae0c896f7d46e7a61b0fd7e2b34dc3}

存在しない場合は、`default::TrustedDomains`から継承されます。

## 関連項目 {#section-2f829671c385411d8e1a7525def5529f}

[src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)、`mask=`、[属性：:RootUrl](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-rooturl.md#reference-b8d706a573814802bd6794223cc78402)

