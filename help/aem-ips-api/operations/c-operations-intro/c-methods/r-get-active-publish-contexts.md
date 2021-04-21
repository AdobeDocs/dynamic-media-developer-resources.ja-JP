---
description: 指定した会社のアクティブな公開コンテキストのリストを取得します。 コンテキストに対して定義されたアクティブなサーバが1つ以上ある場合、パブリッシュコンテキストはアクティブと見なされます。
solution: Experience Manager
title: getActivePublishContext
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 10%

---


# getActivePublishContext{#getactivepublishcontext}

指定した会社のアクティブな公開コンテキストのリストを取得します。 コンテキストに対して定義されたアクティブなサーバが1つ以上ある場合、パブリッシュコンテキストはアクティブと見なされます。

構文

## 認証済みユーザータイプ{#section-eb22397744434dfe92a59ffa2883c2e7}

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
| `*`companyHandle`*` | `xsd:string` | はい | アクティブな公開コンテキストのクエリへの会社のハンドル |

**出力(getActivePublishContextsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`contextArray`*` | `types:StringArray` | はい | アクティブな公開コンテキストの配列です。この中には、公開コンテキストの0個以上の値が含まれる場合があります。 |

