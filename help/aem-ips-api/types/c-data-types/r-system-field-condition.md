---
description: searchAssets操作のシステムフィールド検索条件。
seo-description: searchAssets操作のシステムフィールド検索条件。
seo-title: SystemFieldCondition
solution: Experience Manager
title: SystemFieldCondition
topic: Dynamic Media Image Production System API
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 5%

---


# SystemFieldCondition{#systemfieldcondition}

searchAssets操作のシステムフィールド検索条件。

単項比較の場合、システムフィールドのタイプに応じて1つの値（`boolVal`、`longVal`、`doubleVal`、または`dateVal`）を渡します。 検索範囲の場合は、`min<Type>`パラメーターと`max<Type>`パラメーターを渡し、`Between`または`NotBetween`の`op`値を渡します。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`フィールド`*` | `xsd:string` | アセット検索システムのフィールドの選択を参照してください。 |
| `*`op`*` | `xsd:string` | 文字列比較演算子の選択を参照してください。 |
| `*`value`*` | `xsd:string` | テストの対象となる値。 |
| `*`boolVal`*` | `xsd:boolean` | ブール値の比較値。 |
| `*`longVal`*` | `xsd:long` | 長い比較値。 |
| `*`minLong`*` | `xsd:long` | 長い範囲の下限。 |
| `*`maxLong`*` | `xsd:long` | 長い範囲の上限。 |
| `*`doubleVal`*` | `xsd:double` | 重複比較値。 |
| `*`minDouble`*` | `xsd:double` | 重複範囲の下境界。 |
| `*`maxDouble`*` | `xsd:double` | 重複範囲の上限。 |
| `*`dateVal`*` | `xsd:dateTime` | 日付比較値。 |
| `*`minDate`*` | `xsd:dateTime` | 日付範囲の最小値です。 |
| `*`maxDate`*` | `xsd:dateTime` | 日付範囲の最大値。 |

## 例 {#section-347d4aabfff44530adba03d1dc0b9968}

```
<systemFieldConditionArray>
   <items>
      <field>LastModified</field>
      <op>Between</op>
      <minDate>2007-08-01T00:00:00</minDate>
      <maxDate>2007-12-01T00:00:00</maxDate>
   </items>
</systemFieldConditionArray>
```

