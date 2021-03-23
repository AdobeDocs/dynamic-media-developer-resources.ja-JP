---
description: 画像セット内のメンバの配列を取得します。
seo-description: 画像セット内のメンバの配列を取得します。
seo-title: getImageSetMembers
solution: Experience Manager
title: getImageSetMembers
uuid: b19c9fec-df92-42e1-9228-42cdf196fdfc
feature: Dynamic Mediaクラシック，SDK/API，画像セット
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 13%

---


# getImageSetMembers{#getimagesetmembers}

画像セット内のメンバの配列を取得します。

構文

## 認証済みユーザータイプ{#section-eaa3a167fa77403ea1b374b05fff4ded}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>画像およびメンバセットのアセットに対する読み取りアクセス権が必要です。

## パラメータ {#section-a67ba98095574533980997c83ceaa316}

**入力(getImageSetMembersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 画像セットを含む会社へのハンドル。 |
| `*`assetHandle`*` | `xsd:string` | はい | 画像セットのアセットハンドル。 |

**出力(getImageSetMembersReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`memberArray`*` | `types:ImageSetMemberArray` | いいえ | 画像セットメンバの配列。 |

## 例 {#section-888a9a78033346f39b171229de93dfa0}

このコードのサンプルを使用すると、特定の画像セットメンバーを返すことができます。 応答は空の配列を返します。

**リクエスト**

```java
<ns1:getImageSetMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>34195|22|927</ns1:assetHandle>
</ns1:getImageSetMembersParam>
```

**応答**

```java
<getImageSetMembersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <memberArray></memberArray>
</getImageSetMembersReturn>
```

