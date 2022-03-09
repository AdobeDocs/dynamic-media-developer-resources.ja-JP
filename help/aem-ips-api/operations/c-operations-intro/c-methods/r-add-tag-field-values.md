---
description: 既存のタグフィールドの辞書に新しいタグ値を追加します。
solution: Experience Manager
title: addTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 099263e4-8214-46eb-898e-7a28c4f25598
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 14%

---

# addTagFieldValues{#addtagfieldvalues}

既存のタグフィールドの辞書に新しいタグ値を追加します。

構文

## 認証済みユーザータイプ {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**入力 (addTagFieldValuesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | タグフィールドを含む会社のハンドル。 |
| fieldHandle | `xsd:string` | はい | 変更するタグフィールドのハンドル。 |
| valueArray | `xsd:string` | はい | フィールドの既存の辞書に追加するタグ値の配列。 |

**出力 (addTagFieldValuesParam)**

IPS API はこの操作に対する応答を返しません。

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
