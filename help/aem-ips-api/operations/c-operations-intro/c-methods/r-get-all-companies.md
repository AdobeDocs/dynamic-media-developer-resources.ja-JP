---
description: すべての会社の配列を返します。
seo-description: すべての会社の配列を返します。
seo-title: getAllCompanies
solution: Experience Manager
title: getAllCompanies
topic: Scene7 Image Production System API
uuid: bc2d82b1-e020-4dfe-9704-601ef5aa2111
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 19%

---


# getAllCompanies{#getallcompanies}

すべての会社の配列を返します。

構文

## 認証済みユーザータイプ{#section-773db3753b4842e5a4623ad810176508}

* `IpsAdmin`

## パラメータ {#section-efd74992e6904ebabe7383b577af4fdb}

**入力(getAllCompaniesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`includeExpired`*` | `xsd:boolean` | はい | 期限切れの会社と期限切れでないユーザーを返す場合はtrueに設定します。 |

**Output (getAllCompaniesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyArray`*` | `types:CompanyArray` | はい | 会社の配列。 |

## 例 {#section-3eecf4e6900b41fb92a0e3214791c6b9}

このコードの例では、配列内のIPS内のすべての会社を返します。 ただし、サンプルの応答は簡潔にするために切り捨てられます。

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

