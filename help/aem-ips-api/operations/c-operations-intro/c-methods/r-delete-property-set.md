---
description: プロパティセットおよび関連するすべてのプロパティを削除します。
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 72429030-200d-4e13-a537-10a728998a26
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 13%

---

# deletePropertySet{#deletepropertyset}

プロパティセットおよび関連するすべてのプロパティを削除します。

構文

## 認証済みユーザータイプ {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-e5fc868f69494cf6858e03027db09101}

**入力 (deletePropertySetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| setHandle | `xsd:string` | はい | 削除するプロパティセットへのハンドル。 |

**出力 (deletePropertySetParam)**

IPS API はこの操作に対する応答を返しません。

## 例 {#section-cf319fc8f86a40ab9cbd838b031973fe}

このコード例では、セットのハンドルを `deletePropertySetParam` を IPS Web サービスサーバに送信して、プロパティセットを削除します。

**リクエスト**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**応答**

なし
