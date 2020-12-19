---
description: 指定した会社のアクティブな公開コンテキストのリストを取得します。 コンテキストに対して定義されたアクティブなサーバが1つ以上ある場合、パブリッシュコンテキストはアクティブと見なされます。
seo-description: 指定した会社のアクティブな公開コンテキストのリストを取得します。 コンテキストに対して定義されたアクティブなサーバが1つ以上ある場合、パブリッシュコンテキストはアクティブと見なされます。
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
topic: Scene7 Image Production System API
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 8%

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
| ` *`companyHandle`*` | `xsd:string` | はい | アクティブな公開コンテキストのクエリへの会社のハンドル |

**出力(getActivePublishContextsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`contextArray`*` | `types:StringArray` | はい | アクティブな公開コンテキストの配列です。この中には、公開コンテキストの0個以上の値が含まれる場合があります。 |

