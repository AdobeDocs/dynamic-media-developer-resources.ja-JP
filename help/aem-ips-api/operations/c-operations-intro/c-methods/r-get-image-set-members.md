---
description: 画像セット内のメンバーの配列を取得します。
solution: Experience Manager
title: getImageSetMembers
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,Admin
exl-id: 29ceef8b-127f-4460-8623-c3e26c959327
TQID: 'https://experienceleague.adobe.com/7tS3wEIqaBPmykuVmDBfq9GugDcbnevj-XAQQHM3icY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 13%

---

# getImageSetMembers{#getimagesetmembers}

画像セット内のメンバーの配列を取得します。

構文

## 承認済みユーザータイプ {#section-eaa3a167fa77403ea1b374b05fff4ded}

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
>画像およびメンバーセットアセットへの読み取りアクセスが必要です。

## パラメーター {#section-a67ba98095574533980997c83ceaa316}

**入力（getImageSetMembersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 画像セットを含む会社へのハンドル。 |
| assetHandle | `xsd:string` | はい | 画像セットのアセットハンドル。 |

**出力（getImageSetMembersReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| memberArray | `types:ImageSetMemberArray` | いいえ | 画像セットメンバーの配列。 |

## 例 {#section-888a9a78033346f39b171229de93dfa0}

このコードサンプルは、特定の画像セットメンバーを返します。 応答は空の配列を返します。

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
