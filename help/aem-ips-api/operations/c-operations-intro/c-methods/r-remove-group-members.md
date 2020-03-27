---
description: 特定のグループから会社のユーザーを削除します。
seo-description: 特定のグループから会社のユーザーを削除します。
seo-title: removeGroupMembers
solution: Experience Manager
title: removeGroupMembers
topic: Scene7 Image Production System API
uuid: dd0ea335-bbd0-43b1-830b-77f32dc39b12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# removeGroupMembers{#removegroupmembers}

特定のグループから会社のユーザーを削除します。

**削除コマンドの違い**

* `removeGroupMembers`:グループから複数のユーザーを削除します。
* `removeGroupMembership`:グループの配列から個々のユーザーを削除します。

## 認証されたユーザータイプ {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-b5596614a3be4ce5962455884e4636af}

**入力(removeGroupMembersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 操作するユーザーを含む会社へのハンドル。 |
| ` *`groupHandle`*` | `xsd:string` | はい | グループハンドル。 |
| ` *`userHandleArray`*` | `types:HandleArray` | はい | グループメンバーシップを削除するユーザーのハンドルの配列です。 |

**出力(removeGroupMembersParam)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-9eedac852cea46ec80de6a6928bf97ac}

このコード例では、指定した会社からユーザーを削除します。 ユーザーハンドル配列を持つグループから複数のユーザーを削除します。

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
