---
description: 画像セット内のメンバの配列を取得します。
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 15%

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

