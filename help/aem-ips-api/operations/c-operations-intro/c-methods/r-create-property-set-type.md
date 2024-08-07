---
description: プロパティ セット タイプは、プロパティ セットの管理に役立つ各種の設定を指定します。
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 10%

---

# createPropertySetType{#createpropertysettype}

プロパティ セット タイプは、プロパティ セットの管理に役立つ各種の設定を指定します。

構文

## 許可されているユーザータイプ {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-43dece72eb9f44df80f4a119dd2c008b}

**入力（createPropertySetTypeParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | いいえ | プロパティ セット タイプを所有する会社へのハンドル。 `companyHandle` が渡されず、呼び出し元が `IpsAdmin` の場合は、グローバルプロパティセットタイプが作成されます。 |
| name | `xsd:string` | はい | プロパティセットタイプの名前。 |
| propertyType | `xsd:string` | はい | プロパティセットのタイプを選択します。 |
| allowMultiple | `xsd:boolean` | はい | プログラムが複数のプロパティ セットを持つことができるかどうかを決定します。 |

**Output （createPropertySetTypeReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| typeHandle | `xsd:string` | はい | 型へのハンドル。 |

## 例 {#section-13396c9639a6475190e622eae3cdb534}

このコード例では、`PropertySet Types` 定数で指定された名前と型を持つプロパティ セットを作成します。 プロパティ セット タイプを所有する会社へのハンドル。 companyHandle が渡されず、呼び出し元が IpsAdmin の場合、グローバルプロパティセットタイプが作成されます。

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
