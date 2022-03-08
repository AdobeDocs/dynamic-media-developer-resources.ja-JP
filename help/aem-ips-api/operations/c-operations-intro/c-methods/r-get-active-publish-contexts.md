---
description: 指定した会社のアクティブな公開コンテキストのリストを取得します。 コンテキストに対して 1 つ以上のアクティブなサーバーが定義されている場合、公開コンテキストはアクティブと見なされます。
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 11%

---

# getActivePublishContext{#getactivepublishcontext}

指定した会社のアクティブな公開コンテキストのリストを取得します。 コンテキストに対して 1 つ以上のアクティブなサーバーが定義されている場合、公開コンテキストはアクティブと見なされます。

構文

## 認証済みユーザータイプ {#section-eb22397744434dfe92a59ffa2883c2e7}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-a4be4024e55c472fa6728faec9c5e048}

**入力 (getActivePublishContextsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | アクティブな公開コンテキストをクエリする会社へのハンドル |

**出力 (getActivePublishContextsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| contextArray | `types:StringArray` | はい | アクティブな公開コンテキストの配列。公開コンテキストの 0 個以上の値を含めることができます。 |
