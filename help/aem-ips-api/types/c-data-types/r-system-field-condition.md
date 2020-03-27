---
description: searchAssets操作のシステムフィールド検索条件。
seo-description: searchAssets操作のシステムフィールド検索条件。
seo-title: SystemFieldCondition
solution: Experience Manager
title: SystemFieldCondition
topic: Scene7 Image Production System API
uuid: 811095df-732d-48a3-a6ff-55d6dc602b54
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# SystemFieldCondition{#systemfieldcondition}

searchAssets操作のシステムフィールド検索条件。

単項比較の場合、システムのフィールドの `boolVal`種類に応 `longVal`じて、 `doubleVal`値(、、 `dateVal`、または)を1つだけ渡します。 検索範囲の場合は、パラメ `min<Type>` ーターと `max<Type>` パラメーターを渡し、ま `op` たはの値を渡 `Between` しま `NotBetween`す。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| ` *`フィールド`*` | `xsd:string` | アセット検索システムフィールドの選択を参照してください。 |
| ` *`op`*` | `xsd:string` | 文字列比較演算子の選択を参照してください。 |
| ` *`value`*` | `xsd:string` | テストする値。 |
| ` *`boolVal`*` | `xsd:boolean` | ブール値の比較値。 |
| ` *`longVal`*` | `xsd:long` | 長い比較値。 |
| ` *`minLong`*` | `xsd:long` | 長い範囲の下限。 |
| ` *`maxLong`*` | `xsd:long` | 長い範囲の上限。 |
| ` *`doubleVal`*` | `xsd:double` | 二重比較値。 |
| ` *`minDouble`*` | `xsd:double` | 倍射範囲の下境界。 |
| ` *`maxDouble`*` | `xsd:double` | 二重範囲の上限。 |
| ` *`dateVal`*` | `xsd:dateTime` | 日付比較値。 |
| ` *`minDate`*` | `xsd:dateTime` | 日付範囲の最小値。 |
| ` *`maxDate`*` | `xsd:dateTime` | 最大日付範囲。 |

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

