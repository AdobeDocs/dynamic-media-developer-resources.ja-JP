---
description: プロパティセットとすべての関連プロパティを削除します。
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 12%

---


# deletePropertySet{#deletepropertyset}

プロパティセットとすべての関連プロパティを削除します。

構文

## 認証済みユーザータイプ{#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-e5fc868f69494cf6858e03027db09101}

**入力(deletePropertySetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`setHandle`*` | `xsd:string` | はい | 削除するプロパティセットのハンドル。 |

**出力(deletePropertySetParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-cf319fc8f86a40ab9cbd838b031973fe}

このコードの例では、プロパティセットを削除するために、セットのハンドルをIPS Webサービスサーバーに送信される`deletePropertySetParam`内のフィールドとして使用します。

**リクエスト**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**応答**

なし
