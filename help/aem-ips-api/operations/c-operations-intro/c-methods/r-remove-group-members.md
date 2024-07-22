---
description: 会社のユーザーを特定のグループから削除します。
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 7%

---

# removeGroupMembers{#removegroupmembers}

会社のユーザーを特定のグループから削除します。

**削除コマンドの違い**

* `removeGroupMembers`: グループから複数のユーザーを削除します。
* `removeGroupMembership`：グループの配列から個々のユーザーを削除します。

## 許可されているユーザータイプ {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-b5596614a3be4ce5962455884e4636af}

**入力（removeGroupMembersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 操作するユーザーを含む会社のハンドル。 |
| groupHandle | `xsd:string` | はい | グループハンドル。 |
| userHandleArray | `types:HandleArray` | はい | グループメンバーシップを削除するユーザーのハンドルの配列。 |

**出力（removeGroupMembersParam）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-9eedac852cea46ec80de6a6928bf97ac}

このコードサンプルでは、指定した会社からユーザーを削除します。 ユーザーハンドル配列を持つグループから複数のユーザーを削除します。

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
