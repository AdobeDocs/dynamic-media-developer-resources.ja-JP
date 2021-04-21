---
description: 会社の構造（ファイル数など）に関する情報を返します。
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 13%

---


# getDiskUsage{#getdiskusage}

会社の構造（ファイル数など）に関する情報を返します。

## 認証済みユーザータイプ{#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**入力(getDiskUsageParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | ディスク使用量を取得する会社のハンドル。 |

**出力(getDiskUsageReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`diskUsageArray`*` | `types:DiskUsageArray` | はい | 会社ディスク使用の配列。 |

## 例 {#section-cb16a97badc94076ad5da277db5ed16a}

この要求の名前は誤った結果になります。 会社が使用しているディスク領域の量を反映するスカラ値を返すのではなく、会社の構造に関するその他の情報も取得します。

**リクエスト**

```java
<ns1:getDiskUsageParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
</ns1:getDiskUsageParam>
```

**応答**

```java
<getDiskUsageReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <diskUsageArray>
      <items>
         <companyHandle>47</companyHandle>
         <companyName>My Company</companyName>
         <imageCount>207</imageCount>
         <diskSpaceUsage>3024</diskSpaceUsage>
         <lastModified>2007-09-14T22:10:30.661-07:00</lastModified>
      </items>
   </diskUsageArray>
</getDiskUsageReturn>
```

