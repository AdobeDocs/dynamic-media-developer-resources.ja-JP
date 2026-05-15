---
description: 1つ以上のタグフィールドに定義されているすべてのタグディクショナリ値を取得します。
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 12836783-4f9d-41d3-9b42-6e25238d7ed5
TQID: 'https://experienceleague.adobe.com/b7chzlIT9c4eWbl-MEVgdmvpymwnOieDHgm3a-lMnH4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 85
ht-degree: 15%

---

# getTagFieldValues{#gettagfieldvalues}

1つ以上のタグフィールドに定義されているすべてのタグディクショナリ値を取得します。

構文

## 承認済みユーザータイプ {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメーター {#section-9ad806e7736e4d51ae42cad185050cf9}

**入力（getTagFieldValuesReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | タグフィールドを含む会社のハンドル。 |
| fieldHandleArray | `types:HandleArray` | はい | 返す値をタグ付けするためのフィールドハンドルの配列。 |

**出力（getTagFieldValuesReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| fieldArray | `types:TagFieldValuesArray` | はい | リクエストされた各フィールドの辞書のタグ値の配列。 |

## 例 {#section-4492742614e44bb191a7d397dc1a1407}

**リクエスト**

```java
<getTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandleArray>
      <items>m|3|ASSET|SingleOpenTag</items>
      <items>m|3|ASSET|SingleFixedTag</items>
   </fieldHandleArray>
</getTagFieldValuesParam>
```

**応答**

```java
<getTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <fieldArray>
      <items>
         <fieldHandle>m|3|ASSET|SingleOpenTag</fieldHandle>
         <valueArray>
            <items>GroupB</items>
            <items>GroupA</items>
         </valueArray>
      </items>
      <items>
         <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
         <valueArray>
            <items>North</items>
            <items>South</items>
            <items>East</items><items>West</items>
         </valueArray>
      </items>
   </fieldArray>
</getTagFieldValuesReturn>
```
