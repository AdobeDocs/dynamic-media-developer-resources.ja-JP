---
description: プロパティセットタイプは、プロパティセットの管理に使用する各種設定を指定します。
seo-description: プロパティセットタイプは、プロパティセットの管理に使用する各種設定を指定します。
seo-title: createPropertySetType
solution: Experience Manager
title: createPropertySetType
topic: Scene7 Image Production System API
uuid: ecbaad48-d725-4f7a-a37d-5e4cde3295cb
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createPropertySetType{#createpropertysettype}

プロパティセットタイプは、プロパティセットの管理に使用する各種設定を指定します。

構文

## 認証されたユーザータイプ {#section-48e5f908276c4a549fd33a8828bad326}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-43dece72eb9f44df80f4a119dd2c008b}

**入力(createPropertySetTypeParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | いいえ | プロパティセットタイプを所有する会社のハンドル。 が渡さ `companyHandle` れず、呼び出し元がになっている場合は、グ `IpsAdmin`ローバルプロパティセットタイプが作成されます。 |
| ` *`name`*` | `xsd:string` | はい | プロパティセットタイプの名前。 |
| ` *`propertyType`*` | `xsd:string` | はい | プロパティセットタイプの選択。 |
| ` *`allowMultiple`*` | `xsd:boolean` | はい | プログラムが複数のプロパティセットを持つことができるかどうかを指定します。 |

**出力(createPropertySetTypeReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`typeHandle`*` | `xsd:string` | はい | タイプのハンドル。 |

## 例 {#section-13396c9639a6475190e622eae3cdb534}

このコード例では、定数で指定された名前とタイプを持つプロパティセットを作成 `PropertySet Types` します。 プロパティセットタイプを所有する会社のハンドル。 companyHandleが渡されず、呼び出し元がIpsAdminの場合、グローバルプロパティセットの種類が作成されます。

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

