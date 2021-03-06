---
description: 既存のタグフィールドのタグ辞書の値を設定します。
solution: Experience Manager
title: setTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 50f437d6-fec5-4961-884e-fdb75d201ab7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 16%

---

# setTagFieldValues{#settagfieldvalues}

既存のタグフィールドのタグ辞書の値を設定します。

構文

## 認証済みユーザータイプ {#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-a05cbee4cb4f44198c414a6b14e69156}

**入力**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社の取り扱い。 |
| fieldHandle | `xsd:string` | はい | タグフィールドハンドル。 |
| valueArray | `types:StringArray` | はい | フィールドの既存の辞書を置き換えるタグ値の配列。 新しい値が既存の値と一致する場合、アセットの関連付けは維持されます。 |

**出力 (setTagFieldValuesReturn)**

IPS API はこの操作に対する応答を返しません。

## 例 {#section-b11cafd9bed54ab5836c737cc075c918}

**リクエスト**

```java
<setTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Nurth</items>
      <items>Suth</items>
      <items>East</items>
      <items>West</items>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</setTagFieldValuesParam>
```

**応答**

なし
