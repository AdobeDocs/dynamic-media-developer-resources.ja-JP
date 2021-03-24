---
description: プロパティセットとすべての関連プロパティを削除します。
solution: Experience Manager
title: deletePropertySet
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者，管理者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
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
