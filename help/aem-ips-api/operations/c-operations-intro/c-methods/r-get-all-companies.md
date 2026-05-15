---
description: すべての会社の配列を返します。
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e339ecf-83b5-410c-8683-f3d73bd92339
TQID: 'https://experienceleague.adobe.com/B2wkv6Xvuvg17yqUucjIx170K4YmznQgBrJiVgLe2qg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 71
ht-degree: 16%

---

# getAllCompanies{#getallcompanies}

すべての会社の配列を返します。

構文

## 承認済みユーザータイプ {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## パラメーター {#section-efd74992e6904ebabe7383b577af4fdb}

**Input （getAllCompaniesParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| includeExpired | `xsd:boolean` | はい | 有効期限が切れた会社と期限切れでない会社を返すには、trueに設定します。 |

**出力（getAllCompaniesReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyArray | `types:CompanyArray` | はい | 企業の数。 |

## 例 {#section-3eecf4e6900b41fb92a0e3214791c6b9}

このコードサンプルは、IPSのすべての会社を配列で返します。 注意：サンプル応答は簡潔にするために切り捨てられています。

**リクエスト**

```java
<ns1:getAllCompaniesParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeExpired>false</ns1:includeExpired>
</ns1:getAllCompaniesParam>
```

**応答**

```java
<ns1:getAllCompaniesReturnxmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyArray>
      <ns1:items>
         <ns1:companyHandle>18</ns1:companyHandle>
         <ns1:name>00webload</ns1:name>
         <ns1:rootPath>00webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.667Z</ns1:expires>
      </ns1:items>
      <ns1:items>
         <ns1:companyHandle>19</ns1:companyHandle>
         <ns1:name>01webload</ns1:name>
         <ns1:rootPath>01webload/</ns1:rootPath>
         <ns1:expires>2101-02-01T07:00:00.414Z</ns1:expires>
      </ns1:items>
      . . .
   </ns1:companyArray>
</ns1:getAllCompaniesReturn>
```
