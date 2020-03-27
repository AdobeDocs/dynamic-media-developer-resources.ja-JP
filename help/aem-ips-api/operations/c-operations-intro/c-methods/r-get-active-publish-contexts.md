---
description: 指定した会社のアクティブな公開コンテキストのリストを取得します。 コンテキストに対して少なくとも1つのアクティブなサーバが定義されている場合、公開コンテキストはアクティブと見なされます。
seo-description: 指定した会社のアクティブな公開コンテキストのリストを取得します。 コンテキストに対して少なくとも1つのアクティブなサーバが定義されている場合、公開コンテキストはアクティブと見なされます。
seo-title: getActivePublishContext
solution: Experience Manager
title: getActivePublishContext
topic: Scene7 Image Production System API
uuid: 856704d1-e97b-4d2d-b80c-620450b78432
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getActivePublishContext{#getactivepublishcontext}

指定した会社のアクティブな公開コンテキストのリストを取得します。 コンテキストに対して少なくとも1つのアクティブなサーバが定義されている場合、公開コンテキストはアクティブと見なされます。

構文

## 認証されたユーザータイプ {#section-eb22397744434dfe92a59ffa2883c2e7}

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
| ` *`companyHandle`*` | `xsd:string` | はい | アクティブな発行コンテキストを照会する会社のハンドル |

**出力(getActivePublishContextsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`contextArray`*` | `types:StringArray` | はい | アクティブなパブリッシュコンテキストの配列。パブリッシュコンテキストの0個以上の値を含む場合があります。 |

