---
description: 特定のグループから会社ユーザーを削除します。
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 9%

---


# removeGroupMembers{#removegroupmembers}

特定のグループから会社ユーザーを削除します。

**削除コマンドの違い**

* `removeGroupMembers`:グループから複数のユーザーを削除します。
* `removeGroupMembership`:グループの配列から個々のユーザーを削除します。

## 認証済みユーザータイプ{#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-b5596614a3be4ce5962455884e4636af}

**入力(removeGroupMembersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | はい | 操作する会社のユーザーへのハンドル。 |
| `*`groupHandle`*` | `xsd:string` | はい | グループハンドル |
| `*`userHandleArray`*` | `types:HandleArray` | はい | グループメンバーシップを削除するユーザーのハンドルの配列です。 |

**出力(removeGroupMembersParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-9eedac852cea46ec80de6a6928bf97ac}

このコードのサンプルを使用すると、指定した会社からユーザーを削除できます。 ユーザーハンドル配列を持つグループから複数のユーザーを削除します。

**リクエスト**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**応答**

なし
