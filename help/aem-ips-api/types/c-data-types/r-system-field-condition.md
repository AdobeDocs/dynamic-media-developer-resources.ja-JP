---
description: searchAssets操作のシステムフィールド検索条件。
solution: Experience Manager
title: SystemFieldCondition
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: ebd12727-dbb3-40dc-b631-945415331be6
TQID: 'https://experienceleague.adobe.com/dCZl4pLGuG5hHpEq04W-qv8mRWcFiA7PvmzcO7Un-sM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 83717f155466c1b33cab6f1f8830a9fea68c88c5
workflow-type: tm+mt
source-wordcount: 116
ht-degree: 5%

---

# [!DNL SystemFieldCondition]{#systemfieldcondition}

searchAssets操作のシステムフィールド検索条件。

単項比較の場合は、システムフィールドタイプに応じて、1つの値（`boolVal`、`longVal`、`doubleVal`または`dateVal`）を正確に渡します。 検索範囲の場合は、`min<Type>`と`max<Type>`個のパラメーターを渡し、`op`値`Between`または`NotBetween`を渡します。

## パラメーター {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| 名前 | 種類 | 説明 |
|---|---|---|
| フィールド | `xsd:string` | アセット検索システムのフィールドの選択。 |
| op | `xsd:string` | 文字列比較演算子の選択。 |
| value | `xsd:string` | テストする値。 |
| boolVal | `xsd:boolean` | ブール値の比較値。 |
| longVal | `xsd:long` | 長い比較値。 |
| minLong | `xsd:long` | 長距離の下限。 |
| maxLong | `xsd:long` | 長距離範囲の上限です。 |
| doubleVal | `xsd:double` | 二重比較値。 |
| minDouble | `xsd:double` | 二重範囲の下限。 |
| maxDouble | `xsd:double` | 二重範囲の上限です。 |
| dateVal | `xsd:dateTime` | 日付比較値。 |
| minDate | `xsd:dateTime` | 日付範囲は最小です。 |
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

