---
description: プロパティセットタイプは、プロパティセットの管理に役立つ様々な設定を指定します。
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
TQID: 'https://experienceleague.adobe.com/JOAxK9j-P0v8inQRU65C2rVCM9-OnXTXCF6wtp6eksY'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 156
ht-degree: 10%

---

# createPropertySetType{#createpropertysettype}

プロパティセットタイプは、プロパティセットの管理に役立つ様々な設定を指定します。

構文

## 承認済みユーザータイプ {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-43dece72eb9f44df80f4a119dd2c008b}

**入力（createPropertySetTypeParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | いいえ | プロパティ セット タイプを所有する会社へのハンドル。 `companyHandle`が渡されず、呼び出し元が`IpsAdmin`の場合、グローバル プロパティ セット タイプが作成されます。 |
| name | `xsd:string` | はい | プロパティセットタイプの名前。 |
| propertyType | `xsd:string` | はい | プロパティセットタイプの選択。 |
| allowMultiple | `xsd:boolean` | はい | プログラムに複数のプロパティセットを含めることができるかどうかを指定します。 |

**出力（createPropertySetTypeReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| typeHandle | `xsd:string` | はい | 型へのハンドル。 |

## 例 {#section-13396c9639a6475190e622eae3cdb534}

このコードのサンプルでは、`PropertySet Types`定数で指定された名前と型を持つプロパティ セットを作成します。 プロパティ セット タイプを所有する会社へのハンドル。 companyHandleが渡されず、呼び出し元がIpsAdminの場合、グローバルプロパティセットタイプが作成されます。

**リクエスト**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10803</typeHandle>
</createPropertySetTypeReturn>
```

**応答**

```java
<createPropertySetTypeReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</createPropertySetTypeReturn>
```

