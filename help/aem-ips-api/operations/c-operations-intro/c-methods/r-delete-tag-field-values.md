---
description: タグフィールドのディクショナリからタグフィールドの値を削除します。
seo-description: タグフィールドのディクショナリからタグフィールドの値を削除します。
seo-title: deleteTagFieldValues
solution: Experience Manager
title: deleteTagFieldValues
topic: Scene7 Image Production System API
uuid: 71cdec4e-c1d6-4518-87ed-5c47a5112b15
translation-type: tm+mt
source-git-commit: b5eaefb375fbd0d0786619fa6d84b4f6fc17a77f

---


# deleteTagFieldValues{#deletetagfieldvalues}

タグフィールドのディクショナリからタグフィールドの値を削除します。

## 認証されたユーザータイプ {#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-5db64a6ae238426395bc760b83587260}

**入力(deleteTagFieldValuesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | タグフィールドを含む会社のハンドル。 |
| ` *`fieldHandle`*` | `xsd:string` | はい | 変更するタグフィールドのハンドル。 |
| ` *`valueArray`*` | `types:StringArray` | はい | フィールドのディクショナリから削除するタグ値の配列。 |

**出力(deleteTagFieldValuesParam)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-92f9e575a6da491caa09e264b4d6ee55}

**リクエスト**

```java
deleteTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <valueArray>
      <items>Pineapple</items>
      <items>Banana</items>
   </valueArray>
</deleteTagFieldValuesParam>
```

**応答**

なし
