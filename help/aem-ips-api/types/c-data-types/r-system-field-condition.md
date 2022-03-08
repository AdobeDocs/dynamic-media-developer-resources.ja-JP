---
description: searchAssets 操作のシステムフィールド検索条件。
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 6%

---

# SystemFieldCondition{#systemfieldcondition}

searchAssets 操作のシステムフィールド検索条件。

単項比較の場合、1 つの値 ( `boolVal`, `longVal`, `doubleVal`または `dateVal`) を指定します。 検索範囲の場合は、 `min<Type>` および `max<Type>` パラメーターと `op` 値 `Between` または `NotBetween`.

## パラメータ {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| フィールド | `xsd:string` | アセット検索システムフィールドの選択。 |
| op | `xsd:string` | 文字列比較演算子の選択。 |
| value | `xsd:string` | テストする値。 |
| boolVal | `xsd:boolean` | ブール値比較値。 |
| longVal | `xsd:long` | 長い比較値。 |
| minLong | `xsd:long` | 長い範囲の下の境界。 |
| maxLong | `xsd:long` | 長い範囲の上限。 |
| doubleVal | `xsd:double` | 二重比較値。 |
| minDouble | `xsd:double` | 二重範囲の下の境界。 |
| maxDouble | `xsd:double` | 二重範囲の上の境界。 |
| dateVal | `xsd:dateTime` | 日付比較値。 |
| minDate | `xsd:dateTime` | 日付範囲の最小値。 |
| maxDate | `xsd:dateTime` | 日付範囲の最大値。 |

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
