---
description: タグフィールドの辞書からタグフィールドの値を削除します。
solution: Experience Manager
title: deleteTagFieldValues
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 12%

---


# deleteTagFieldValues{#deletetagfieldvalues}

タグフィールドの辞書からタグフィールドの値を削除します。

## 認証済みユーザータイプ{#section-e6f97c875c2a4cf0a7bc22096b649497}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-5db64a6ae238426395bc760b83587260}

**Input (deleteTagFieldValuesParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | タグフィールドを含む会社のハンドル。 |
| `*`fieldHandle`*` | `xsd:string` | はい | 変更するタグフィールドのハンドル。 |
| `*`valueArray`*` | `types:StringArray` | はい | フィールドのディクショナリから削除するタグ値の配列。 |

**出力(deleteTagFieldValuesParam)**

IPS APIは、この操作に対する応答を返しません。

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
