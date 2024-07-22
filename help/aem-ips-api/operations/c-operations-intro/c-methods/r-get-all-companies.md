---
description: すべての会社の配列を返します。
solution: Experience Manager
title: getAllCompanies
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0e339ecf-83b5-410c-8683-f3d73bd92339
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '70'
ht-degree: 17%

---

# getAllCompanies{#getallcompanies}

すべての会社の配列を返します。

構文

## 許可されているユーザータイプ {#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## パラメーター {#section-efd74992e6904ebabe7383b577af4fdb}

**入力（getAllCompaniesParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| includeExpired | `xsd:boolean` | はい | true に設定すると、期限切れの会社と期限切れでない会社が返されます。 |

**出力（getAllCompaniesReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyArray | `types:CompanyArray` | はい | 会社の配列。 |

## 例 {#section-3eecf4e6900b41fb92a0e3214791c6b9}

このコードサンプルでは、IPS 内のすべての会社を配列で返します。 なお、簡潔にするために、サンプルの応答は切り捨てられます。

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
