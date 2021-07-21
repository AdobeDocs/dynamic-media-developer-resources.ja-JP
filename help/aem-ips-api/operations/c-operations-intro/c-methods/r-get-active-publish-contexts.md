---
description: 指定された会社のアクティブな公開コンテキストのリストを取得します。 コンテキストに対して1つ以上のアクティブなサーバーが定義されている場合、パブリッシュコンテキストはアクティブと見なされます。
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 9f450263-6877-4b32-a71a-8f67b0537a69
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 10%

---

# getActivePublishContext{#getactivepublishcontext}

指定された会社のアクティブな公開コンテキストのリストを取得します。 コンテキストに対して1つ以上のアクティブなサーバーが定義されている場合、パブリッシュコンテキストはアクティブと見なされます。

構文

## 許可されたユーザーの種類 {#section-eb22397744434dfe92a59ffa2883c2e7}

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

**入力(getActivePublishContextsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | アクティブな公開コンテキストをクエリする会社へのハンドル |

**出力(getActivePublishContextsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | はい | アクティブな公開コンテキストの配列。パブリッシュコンテキストの0個以上の値を含めることができます。 |
