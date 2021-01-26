---
description: 既存のタグフィールドの辞書に新しいタグ値を追加します。
solution: Experience Manager
title: addTagFieldValues
topic: Dynamic Media Image Production System API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 14%

---


# addTagFieldValues{#addtagfieldvalues}

既存のタグフィールドの辞書に新しいタグ値を追加します。

構文

## 認証済みユーザータイプ{#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**Input (addTagFieldValuesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | タグフィールドを含む会社のハンドル。 |
| `*`fieldHandle`*` | `xsd:string` | はい | 変更するタグフィールドのハンドル。 |
| `*`valueArray`*` | `xsd:string` | はい | フィールドの既存の辞書に追加するタグ値の配列です。 |

**出力(addTagFieldValuesParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-c4049392f1c548f883b8b1f8f167bada}

**リクエスト**

```java
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
