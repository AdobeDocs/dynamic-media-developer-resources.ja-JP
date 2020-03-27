---
description: 画像形式を作成します。
seo-description: 画像形式を作成します。
seo-title: saveImageFormat
solution: Experience Manager
title: saveImageFormat
topic: Scene7 Image Production System API
uuid: b11ea668-7a82-439c-b16b-909dc86c00a2
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveImageFormat{#saveimageformat}

画像形式を作成します。

>[!NOTE]
>
>フィールド `urlModifier` 値は、有効なXMLで構成されている必要があります。 例えば、をに変更し `&` ます `&`。 IPSユーザイ `urlModfier` ンターフェイスから値を取得します。

## 認証されたユーザータイプ {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**Input (saveImageFormatParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 操作する画像形式を持つ会社のハンドル。 |
| ` *`imageFormatHandle`*` | `xsd:string` | いいえ | 保存する画像形式のハンドル。 |
| ` *`name`*` | `xsd:string` | はい | 画像形式名。 |
| ` *`urlModifier`*` | `xsd:string` | はい | 任意のIPSプロトコルクエリ文字列を指定できます。 URL修飾子を生成する最も簡単な方法は、IPSユーザインターフェイスを使用してURL修飾子を作成し、クエリ文字列を切り取って貼り付けることです。 |

**出力(saveImageFormatReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`imageFormatHandle`*` | `xsd:string` | はい | 画像形式のハンドル。 |

## 例 {#section-c7bd733212ef494297a97093f3af193f}

このコードサンプルを使用して、画像形式を作成します。 この例では、はIPSユ `urlModifier` ーザインターフェイスの値と有効なHTML形式で決定されています。

**リクエスト**

```java
<saveImageFormatParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <name>My Image Format Name</name> 
   <urlModifier>wid=400&amp;hei=400&amp;fmt=jpeg&amp;qlt=750&amp;op_sharpen=0&amp; 
   resMode=bicub&amp;op_usm=0.0,0.0,0,0&amp;iccEmbed=0 
   </urlModifier> 
</saveImageFormatParam>
```

**応答**

```java
<saveImageFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageFormatHandle>47|301</imageFormatHandle> 
</saveImageFormatReturn>
```

