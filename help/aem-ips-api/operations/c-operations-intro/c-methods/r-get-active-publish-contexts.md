---
description: 指定した会社のアクティブな公開コンテキストのリストを取得します。 公開コンテキストに少なくとも1つのアクティブなサーバーが定義されている場合、公開コンテキストはアクティブと見なされます。
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
TQID: 'https://experienceleague.adobe.com/g337PVX5asvB-o-VQL0XA5XSrgQ0c2vx0xC4-93Dm8E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 10%

---

# getActivePublishContext{#getactivepublishcontext}

指定した会社のアクティブな公開コンテキストのリストを取得します。 公開コンテキストに少なくとも1つのアクティブなサーバーが定義されている場合、公開コンテキストはアクティブと見なされます。

構文

## 承認済みユーザータイプ {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-a4be4024e55c472fa6728faec9c5e048}

**入力（getActivePublishContextsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | アクティブな公開コンテキストについてクエリを実行する会社へのハンドル |

**出力（getActivePublishContextsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| contextArray | `types:StringArray` | はい | パブリッシュコンテキストのアクティブな配列。パブリッシュコンテキストの0以上の値を含めることができます。 |
