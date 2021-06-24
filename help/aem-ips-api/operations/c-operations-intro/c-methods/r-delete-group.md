---
description: グループを削除します。
solution: Experience Manager
title: deleteGroup
feature: Dynamic Media Classic、SDK/API
role: Developer,Administrator
exl-id: 0de188de-b4b6-4f48-9918-bcf962fa9482
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 13%

---

# deleteGroup{#deletegroup}

グループを削除します。

構文

## 許可されたユーザーの種類 {#section-ebcc67723663494db0562275b1873460}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-42775102ec724c36ae5241eea1a00b8e}

**入力(deleteGroupParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 削除するグループに属する会社のハンドル。 |
| `*`groupHandle`*` | `xsd:string` | はい | 削除するグループのハンドル。 |

**出力(deleteGroupParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-8f8501af3b3348a1b5701cf9622bf6e4}

このサンプルコードでは、会社からグループを削除します。 別の操作から取得する必要があるグループハンドルが必要です。

**リクエスト**

```java
<ns1:deleteGroupParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>241</ns1:groupHandle>
</ns1:deleteGroupParam>
```

**応答**

なし
