---
description: プロパティセットタイプは、プロパティセットの管理に使用する様々な設定を指定します。
solution: Experience Manager
title: createPropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1730ccbf-e8b0-4f92-9daf-da2fa047cbbd
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 12%

---

# createPropertySetType{#createpropertysettype}

プロパティセットタイプは、プロパティセットの管理に使用する様々な設定を指定します。

構文

## 認証済みユーザータイプ {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-43dece72eb9f44df80f4a119dd2c008b}

**入力 (createPropertySetTypeParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | いいえ | プロパティセットタイプを所有する会社へのハンドル。 If `companyHandle` が渡されておらず、呼び出し元が `IpsAdmin`を指定した場合、グローバルプロパティセットタイプが作成されます。 |
| `*`name`*` | `xsd:string` | はい | プロパティセットタイプの名前。 |
| `*`propertyType`*` | `xsd:string` | はい | プロパティセットタイプの選択。 |
| `*`allowMultiple`*` | `xsd:boolean` | はい | プログラムが複数のプロパティセットを持つことができるかどうかを指定します。 |

**出力 (createPropertySetTypeReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | はい | タイプへのハンドル。 |

## 例 {#section-13396c9639a6475190e622eae3cdb534}

このコード例では、 `PropertySet Types` 定数。 プロパティセットタイプを所有する会社へのハンドル。 companyHandle が渡されず、呼び出し元が IpsAdmin の場合、グローバルプロパティセットの種類が作成されます。

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
