---
description: 既存のタグフィールドにタグディクショナリの値を設定します。
seo-description: 既存のタグフィールドにタグディクショナリの値を設定します。
seo-title: setTagFieldValues
solution: Experience Manager
title: setTagFieldValues
topic: Scene7 Image Production System API
uuid: 56666c00-3694-4a43-a0ff-97af45c8df9f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 14%

---


# setTagFieldValues{#settagfieldvalues}

既存のタグフィールドにタグディクショナリの値を設定します。

構文

## 認証済みユーザータイプ{#section-8b1413654bab44cfb2b1fffbb88aa385}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-a05cbee4cb4f44198c414a6b14e69156}

**入力**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社ハンドル |
| ` *`fieldHandle`*` | `xsd:string` | はい | タグフィールドハンドル。 |
| ` *`valueArray`*` | `types:StringArray` | はい | フィールドの既存の辞書を置き換えるタグ値の配列。 新しい値が既存の値と一致する場合、アセットの関連付けは維持されます。 |

**出力(setTagFieldValuesReturn)**

IPS APIは、この操作に対する応答を返しません。

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
