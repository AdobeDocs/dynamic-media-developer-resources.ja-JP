---
description: 画像形式を作成します。
solution: Experience Manager
title: saveImageFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: cafbd715-237b-4454-920e-643f0c84e208
TQID: 'https://experienceleague.adobe.com/kP25DoK-SIRIYh69I8tE07KH4dI-GFZf9JjUZjG-lFw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 146
ht-degree: 10%

---

# saveImageFormat{#saveimageformat}

画像形式を作成します。

>[!NOTE]
>
>`urlModifier` フィールド値は有効なXMLで構成する必要があります。 例えば、`&`を`&`に変更します。 IPS ユーザーインターフェイスから`urlModfier`値を取得します。

## 承認済みユーザータイプ {#section-12c9d8d5933f4692bafb194060b4f882}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-b1fc2fe8d606490ba3a2c979ab8bbd78}

**入力（saveImageFormatParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 使用する画像形式を持つ会社へのハンドル。 |
| imageFormatHandle | `xsd:string` | いいえ | 保存する画像形式のハンドル。 |
| name | `xsd:string` | はい | 画像フォーマット名。 |
| urlModifier | `xsd:string` | はい | これは、任意のIPS プロトコルクエリ文字列にできます。 URL修飾子を生成する最も簡単な方法は、IPS ユーザーインターフェイスを使用してURL修飾子を作成し、クエリ文字列をカット&amp;ペーストすることです。 |

**出力（saveImageFormatReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| imageFormatHandle | `xsd:string` | はい | 画像フォーマットに対応します。 |

## 例 {#section-c7bd733212ef494297a97093f3af193f}

このコードサンプルは、画像形式を作成します。 この例では、`urlModifier`は、有効なHTML フォーマットを持つIPS ユーザーインターフェイスの値によって決定されました。

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
