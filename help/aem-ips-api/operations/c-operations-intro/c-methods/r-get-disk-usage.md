---
description: 会社の構造に関する情報（ファイル数など）を返します。
solution: Experience Manager
title: getDiskUsage
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 06fdd9f5-5021-4f0b-b312-4465df9bda25
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 10%

---

# getDiskUsage{#getdiskusage}

会社の構造に関する情報（ファイル数など）を返します。

## 許可されているユーザータイプ {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**入力（getDiskUsageParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 取得するディスク使用量の会社に対するハンドル。 |

**出力（getDiskUsageReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| diskUsageArray | `types:DiskUsageArray` | はい | 会社のディスク使用の配列。 |

## 例 {#section-cb16a97badc94076ad5da277db5ed16a}

このリクエストの名前は誤解を招きます。 企業が使用しているディスク容量を反映するスカラー値を返すだけでなく、企業の構造に関する他の情報も取得します。

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
