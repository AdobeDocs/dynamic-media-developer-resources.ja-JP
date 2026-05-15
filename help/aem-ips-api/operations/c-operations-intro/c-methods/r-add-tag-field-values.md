---
description: 既存のタグフィールドの辞書に新しいタグ値を追加します。
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
TQID: 'https://experienceleague.adobe.com/-DA9IYswE5Mfflys-Cn0Gi62OsMU3O1QYIIKYJNq9QU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 11%

---

# addTagFieldValues{#addtagfieldvalues}

既存のタグフィールドの辞書に新しいタグ値を追加します。

構文

## 承認済みユーザータイプ {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**入力（addTagFieldValuesParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | タグフィールドを含む会社のハンドル。 |
| fieldHandle | `xsd:string` | はい | 変更するタグフィールドのハンドル。 |
| valueArray | `xsd:string` | はい | フィールドの既存の辞書に追加するタグ値の配列。 |

**出力（addTagFieldValuesParam）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-c4049392f1c548f883b8b1f8f167bada}

**リクエスト**

```java {.line-numbers}
<addTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</addTagFieldValuesParam>
```

**応答**

なし
