---
description: プロパティセットの種類と、それに関連するプロパティセットおよびプロパティを削除します。
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 11%

---

# deletePropertySetType{#deletepropertysettype}

プロパティセットの種類と、それに関連するプロパティセットおよびプロパティを削除します。

構文

## 許可されたユーザーの種類 {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-1c8973f5d35f44b4a6a483a41609e455}

**入力(deletePropertySetTypeParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`typeHandle`*` | `xsd:string` | はい | 削除するプロパティセットタイプへのハンドル。 |

**出力(deletePropertySetTypeParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-85faa2e3411a4e23aa6489037f7ce078}

このコードサンプルでは、型のハンドルを、IPS Webサービスサーバーに送信される`deletePropertySetTypeParam`のフィールドとして使用して、プロパティセット型を削除します。

**リクエスト**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**応答**

なし
