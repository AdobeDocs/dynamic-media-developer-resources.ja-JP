---
description: グループの配列からユーザーを削除します。
seo-description: グループの配列からユーザーを削除します。
seo-title: removeGroupMembership
solution: Experience Manager
title: removeGroupMembership
topic: Dynamic Media Image Production System API
uuid: 553d91a3-73d6-4323-9436-a3ba13260a6c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 10%

---


# removeGroupMembership{#removegroupmembership}

グループの配列からユーザーを削除します。

**削除コマンドの違い**

* `removeGroupMembers`:グループから複数のユーザーを削除します。
* `removeGroupMembership`:グループの配列から個々のユーザーを削除します。

## 認証済みユーザータイプ{#section-83f3048bbe5a4f62b7b14dc9efdd951a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-d6a15fa70d3d4fc69da200cdaf59904e}

**入力(removeGroupMembershipParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | いいえ | グループメンバーシップを削除する会社のハンドル。 |
| `*`groupHandleArray`*` | `types:HandleArray` | はい | 会社を削除するグループへのハンドルの配列。 |

**出力(removeGroupMembershipReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-f8d4181170a243efb9faf5824ae96197}

このコードの例では、ユーザーをグループから削除します。

**リクエスト**

```java
<ns1:removeGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>47</ns1:userHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:removeGroupMembershipParam>
```

**応答**

なし
