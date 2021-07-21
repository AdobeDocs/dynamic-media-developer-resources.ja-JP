---
description: イメージセット内のメンバの配列を取得します。
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API，画像セット
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 15%

---

# getImageSetMembers{#getimagesetmembers}

イメージセット内のメンバの配列を取得します。

構文

## 許可されたユーザーの種類 {#section-eaa3a167fa77403ea1b374b05fff4ded}

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
>画像とメンバセットのアセットに対する読み取りアクセス権が必要です。

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

このコードサンプルは、特定の画像セットメンバを返します。 応答は空の配列を返します。

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
