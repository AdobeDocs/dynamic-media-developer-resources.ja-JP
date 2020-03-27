---
description: 会社の構造（ファイル数など）に関する情報を返します。
seo-description: 会社の構造（ファイル数など）に関する情報を返します。
seo-title: getDiskUsage
solution: Experience Manager
title: getDiskUsage
topic: Scene7 Image Production System API
uuid: 29190200-8f49-4689-9782-1df665dca1b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getDiskUsage{#getdiskusage}

会社の構造（ファイル数など）に関する情報を返します。

## 認証されたユーザータイプ {#authorized-user-types}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-e7e47082faf44ae28a2cfa7ef53aedbb}

**入力(getDiskUsageParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | ディスク使用量を取得する会社のハンドル。 |

**出力(getDiskUsageReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`diskUsageArray`*` | `types:DiskUsageArray` | はい | 会社のディスク使用のアレイ。 |

## 例 {#section-cb16a97badc94076ad5da277db5ed16a}

この要求の名前は誤った名前になります。 会社が使用しているディスク容量を反映するスカラー値を返すのではなく、会社の構造に関するその他の情報も取得します。

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

