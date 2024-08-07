---
description: 1 つ以上のタグフィールドに定義されているすべてのタグディクショナリ値を取得します。
solution: Experience Manager
title: getTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 12836783-4f9d-41d3-9b42-6e25238d7ed5
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 15%

---

# getTagFieldValues{#gettagfieldvalues}

1 つ以上のタグフィールドに定義されているすべてのタグディクショナリ値を取得します。

構文

## 許可されているユーザータイプ {#section-cc36a437394c491594e704a08a161c87}

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
| fieldHandleArray | `types:HandleArray` | はい | 返すタグ値に対応するフィールドハンドルの配列。 |

**出力（getTagFieldValuesReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| fieldArray | `types:TagFieldValuesArray` | はい | リクエストされた各フィールドのディクショナリのタグ値の配列。 |

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
