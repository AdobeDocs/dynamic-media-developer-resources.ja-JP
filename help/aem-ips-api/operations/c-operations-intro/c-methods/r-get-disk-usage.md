---
description: 会社の構造に関する情報（ファイル数など）を返します。
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 13%

---

# getDiskUsage{#getdiskusage}

会社の構造に関する情報（ファイル数など）を返します。

## 許可されたユーザーの種類 {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**入力(getDiskUsageParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | ディスク使用量を取得する会社へのハンドル。 |

**出力(getDiskUsageReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`diskUsageArray`*` | `types:DiskUsageArray` | はい | 会社のディスク使用のアレイ。 |

## 例 {#section-cb16a97badc94076ad5da277db5ed16a}

このリクエストの名前は誤解を招きます。 会社が使用しているディスク領域を反映するスカラー値を返すのではなく、会社の構造に関する他の情報も取得します。

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
