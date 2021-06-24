---
description: すべての会社の配列を返します。
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: 0e339ecf-83b5-410c-8683-f3d73bd92339
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 20%

---

# getAllCompanies{#getallcompanies}

すべての会社の配列を返します。

構文

## 許可されたユーザーの種類 {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## パラメータ {#section-efd74992e6904ebabe7383b577af4fdb}

**入力(getAllCompaniesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`includeExpired`*` | `xsd:boolean` | はい | 期限切れの会社と期限切れでない会社を返す場合は、trueに設定します。 |

**出力(getAllCompaniesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyArray`*` | `types:CompanyArray` | はい | 会社の配列。 |

## 例 {#section-3eecf4e6900b41fb92a0e3214791c6b9}

このコードサンプルは、IPSのすべての会社を配列で返します。 なお、サンプルの応答は簡潔にするために切り捨てられます。

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
