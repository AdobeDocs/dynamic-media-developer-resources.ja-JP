---
description: searchAssets操作のシステムフィールド検索条件。
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 5%

---

# SystemFieldCondition{#systemfieldcondition}

searchAssets操作のシステムフィールド検索条件。

単項の比較では、システムフィールドのタイプに応じて、1つの値(`boolVal`、`longVal`、`doubleVal`、`dateVal`)を渡します。 検索範囲の場合は、`min<Type>`パラメーターと`max<Type>`パラメーターを渡し、`Between`または`NotBetween`の`op`値を渡します。

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| `*`フィールド`*` | `xsd:string` | アセット検索システムのフィールドの選択。 |
| `*`op`*` | `xsd:string` | 文字列比較演算子の選択。 |
| `*`value`*` | `xsd:string` | テストする値。 |
| `*`boolVal`*` | `xsd:boolean` | ブール値比較値。 |
| `*`longVal`*` | `xsd:long` | 長い比較値。 |
| `*`minLong`*` | `xsd:long` | 長い範囲の下限。 |
| `*`maxLong`*` | `xsd:long` | 長い範囲の上限。 |
| `*`doubleVal`*` | `xsd:double` | 二重比較値。 |
| `*`minDouble`*` | `xsd:double` | ダブル範囲の下限。 |
| `*`maxDouble`*` | `xsd:double` | ダブル範囲の上限。 |
| `*`dateVal`*` | `xsd:dateTime` | 日付比較値。 |
| `*`minDate`*` | `xsd:dateTime` | 最小の日付範囲。 |
| `*`maxDate`*` | `xsd:dateTime` | 最大日付範囲。 |

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
