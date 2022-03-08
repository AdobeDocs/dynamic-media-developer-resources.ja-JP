---
description: 画像形式を作成します。
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 12%

---

# saveImageFormat{#saveimageformat}

画像形式を作成します。

>[!NOTE]
>
>この `urlModifier` フィールドの値は、有効な XML で構成する必要があります。 例えば、 `&` から `&`. を取得 `urlModfier` IPS ユーザインターフェイスの値

## 認証済みユーザータイプ {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**入力 (saveImageFormatParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 操作する画像形式を持つ会社へのハンドル。 |
| imageFormatHandle | `xsd:string` | いいえ | 保存する画像形式ハンドル。 |
| name | `xsd:string` | はい | 画像形式名。 |
| urlModifier | `xsd:string` | はい | IPS プロトコルのクエリー文字列を指定できます。 URL 修飾子を生成する最も簡単な方法は、IPS ユーザーインターフェイスを使用して URL 修飾子を作成し、クエリ文字列を切り取って貼り付けることです。 |

**出力 (saveImageFormatReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | はい | 画像形式を処理します。 |

## 例 {#section-c7bd733212ef494297a97093f3af193f}

このコードサンプルは、画像形式を作成します。 この例では、 `urlModifier` は、有効なHTML形式を持つ IPS ユーザインターフェイスの値によって決定されます。

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
