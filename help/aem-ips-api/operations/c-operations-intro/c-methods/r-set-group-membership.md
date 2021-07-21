---
description: ユーザーのグループメンバーシップを設定します。
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 12%

---

# setGroupMembership{#setgroupmembership}

ユーザーのグループメンバーシップを設定します。

構文

## 許可されたユーザーの種類 {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-6aeda13b26af4796aad1306ac7a9ad17}

**入力(setGroupMembershipParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | いいえ | グループメンバーシップを設定するユーザーのハンドル。 |
| `*`companyHandle`*` | `xsd:string` | いいえ | 会社の担当。 |
| `*`groupHandleArray`*` | `types:HandleArray` | はい | ユーザーが属するグループに対するハンドルの配列。 |

**出力(setGroupMembershipReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-67b86d259df24938896fe19061845811}

このコードのサンプルを使用すると、ユーザーはグループのメンバーになります。 グループハンドル配列を使用して、複数のグループにユーザーを追加します。

**リクエスト**

```java
<ns1:setGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>70|kmagnusson@adobe.com</ns1:userHandle>
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray>
      <ns1:items>225</ns1:items>
   </ns1:groupHandleArray>
</ns1:setGroupMembershipParam>
```

**応答**

なし
