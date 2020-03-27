---
description: プロパティセットとすべての関連プロパティを削除します。
seo-description: プロパティセットとすべての関連プロパティを削除します。
seo-title: deletePropertySet
solution: Experience Manager
title: deletePropertySet
topic: Scene7 Image Production System API
uuid: b4fdf51f-89ec-4a69-9179-078ee8e1937f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# deletePropertySet{#deletepropertyset}

プロパティセットとすべての関連プロパティを削除します。

構文

## 認証されたユーザータイプ {#section-b54aa8c854de400a989b4957412ff42c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-e5fc868f69494cf6858e03027db09101}

**入力(deletePropertySetParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`setHandle`*` | `xsd:string` | はい | 削除するプロパティセットのハンドル。 |

**出力(deletePropertySetParam)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-cf319fc8f86a40ab9cbd838b031973fe}

このコード例では、セットのハンドルをIPS Webサービスサーバに送信され `deletePropertySetParam` るフィールドとして使用し、プロパティセットを削除します。

**リクエスト**

```java
<deletePropertySetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <setHandle>ps|941</setHandle>
</deletePropertySetParam>
```

**応答**

なし
