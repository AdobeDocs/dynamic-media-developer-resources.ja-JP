---
description: 特定のグループから会社ユーザーを削除します。
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
TQID: 'https://experienceleague.adobe.com/dMEOhQgXQvFvZj2Kozsq6J7qJNiwYpknQQbNkADMsg0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 117
ht-degree: 7%

---

# removeGroupMembers{#removegroupmembers}

特定のグループから会社ユーザーを削除します。

**削除コマンドの違い**

* `removeGroupMembers`: グループから複数のユーザーを削除します。
* `removeGroupMembership`: グループの配列から個々のユーザーを削除します。

## 承認済みユーザータイプ {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-b5596614a3be4ce5962455884e4636af}

**入力（removeGroupMembersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 一緒に働きたいユーザーを持つ会社へのハンドル。 |
| groupHandle | `xsd:string` | はい | グループハンドル： |
| userHandleArray | `types:HandleArray` | はい | グループ メンバーシップを削除するユーザーのハンドルの配列。 |

**出力（removeGroupMembersParam）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-9eedac852cea46ec80de6a6928bf97ac}

このコードサンプルは、指定した会社からユーザーを削除します。 ユーザーハンドル配列を持つグループから複数のユーザーを削除します。

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
