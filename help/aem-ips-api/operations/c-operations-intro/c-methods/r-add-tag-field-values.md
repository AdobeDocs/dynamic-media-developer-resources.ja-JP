---
description: 既存のタグフィールドの辞書に新しいタグ値を追加します。
seo-description: 既存のタグフィールドの辞書に新しいタグ値を追加します。
seo-title: addTagFieldValues
solution: Experience Manager
title: addTagFieldValues
topic: Scene7 Image Production System API
uuid: 9304f02c-a1df-4477-ab33-f2491c390c92
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# addTagFieldValues{#addtagfieldvalues}

既存のタグフィールドの辞書に新しいタグ値を追加します。

構文

## 認証されたユーザータイプ {#section-ba1d7040661e48b7a6b035494e065c91}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-abe8893038bb4ddfaccc11a8c75e6bd0}

**入力(addTagFieldValuesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | タグフィールドを含む会社のハンドル。 |
| ` *`fieldHandle`*` | `xsd:string` | はい | 変更するタグフィールドのハンドル。 |
| ` *`valueArray`*` | `xsd:string` | はい | フィールドの既存の辞書に追加するタグ値の配列です。 |

**出力(addTagFieldValuesParam)**

IPS APIはこの操作に対する応答を返しません。

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
