---
description: グループを削除します。
seo-description: グループを削除します。
seo-title: deleteGroup
solution: Experience Manager
title: deleteGroup
topic: Scene7 Image Production System API
uuid: 04934b16-b7ef-4657-9f63-c91fcc741ca4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 13%

---


# deleteGroup{#deletegroup}

グループを削除します。

構文

## 認証済みユーザータイプ{#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-42775102ec724c36ae5241eea1a00b8e}

**入力(deleteGroupParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 削除するグループに属する会社のハンドル。 |
| ` *`groupHandle`*` | `xsd:string` | はい | 削除するグループへのハンドル。 |

**出力(deleteGroupParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-8f8501af3b3348a1b5701cf9622bf6e4}

このサンプルコードは、会社からグループを削除します。 別の操作から取得する必要があるグループハンドルが必要です。

**リクエスト**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**応答**

なし
