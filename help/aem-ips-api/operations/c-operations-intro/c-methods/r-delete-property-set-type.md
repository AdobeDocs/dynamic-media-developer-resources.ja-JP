---
description: プロパティセットの種類、および関連するプロパティセットとプロパティを削除します。
solution: Experience Manager
title: deletePropertySetType
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 97ec0f41-794f-4340-b86d-ab07a742d447
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 11%

---

# deletePropertySetType{#deletepropertysettype}

プロパティセットの種類、および関連するプロパティセットとプロパティを削除します。

構文

## 認証済みユーザータイプ {#section-16a17b4ebf9a4639bdb2784a2e9fe00d}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-1c8973f5d35f44b4a6a483a41609e455}

**入力 (deletePropertySetTypeParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| typeHandle | `xsd:string` | はい | 削除するプロパティセットタイプへのハンドル。 |

**出力 (deletePropertySetTypeParam)**

IPS API はこの操作に対する応答を返しません。

## 例 {#section-85faa2e3411a4e23aa6489037f7ce078}

このコード例では、型のハンドルを `deletePropertySetTypeParam` プロパティセットの種類を削除するために、IPS Web サービスサーバに送信されました。

**リクエスト**

```java
<deletePropertySetTypeParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <typeHandle>pt|10801</typeHandle>
</deletePropertySetTypeParam>
```

**応答**

なし
