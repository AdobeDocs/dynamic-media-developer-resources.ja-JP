---
description: 画像セットに含まれるメンバーの配列を取得します。
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 13%

---

# getImageSetMembers{#getimagesetmembers}

画像セットに含まれるメンバーの配列を取得します。

構文

## 許可されているユーザータイプ {#section-eaa3a167fa77403ea1b374b05fff4ded}

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
>画像およびメンバーセットアセットへの読み取りアクセス権が必要です。

## パラメーター {#section-a67ba98095574533980997c83ceaa316}

**入力（getImageSetMembersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 画像セットを含む会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | 画像セットアセットハンドル。 |

**出力（getImageSetMembersReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| memberArray | `types:ImageSetMemberArray` | いいえ | 画像セットメンバーの配列。 |

## 例 {#section-888a9a78033346f39b171229de93dfa0}

このコードサンプルでは、特定の画像セットメンバーを返します。 応答は、空の配列を返します。

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
