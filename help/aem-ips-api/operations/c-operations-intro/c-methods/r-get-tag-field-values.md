---
description: 1つ以上のタグフィールドに対して定義されているすべてのタグディクショナリ値を取得します。
seo-description: 1つ以上のタグフィールドに対して定義されているすべてのタグディクショナリ値を取得します。
seo-title: getTagFieldValues
solution: Experience Manager
title: getTagFieldValues
topic: Scene7 Image Production System API
uuid: 92d84dfc-6a6c-4876-9670-1152adb6317c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getTagFieldValues{#gettagfieldvalues}

1つ以上のタグフィールドに対して定義されているすべてのタグディクショナリ値を取得します。

構文

## 認証されたユーザータイプ {#section-cc36a437394c491594e704a08a161c87}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## パラメータ {#section-9ad806e7736e4d51ae42cad185050cf9}

**Input (getTagFieldValuesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | タグフィールドを含む会社のハンドル。 |
| ` *`fieldHandleArray`*` | `types:HandleArray` | はい | 返す値にタグを付けるフィールドハンドルの配列。 |

**出力(getTagFieldValuesReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`fieldArray`*` | `types:TagFieldValuesArray` | はい | リクエストされた各フィールドのディクショナリ内のタグ値の配列。 |

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

