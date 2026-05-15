---
description: ユーザーのグループメンバーシップを設定します。
solution: Experience Manager
title: setGroupMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0a355a34-1c2d-48c1-ba12-7d07d1673d09
TQID: 'https://experienceleague.adobe.com/j-wK2g-evSRY0YD3ZspgT--giCkKJl1VBYgPylixVz8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 96
ht-degree: 10%

---

# setGroupMembership{#setgroupmembership}

ユーザーのグループメンバーシップを設定します。

構文

## 承認済みユーザータイプ {#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-6aeda13b26af4796aad1306ac7a9ad17}

**入力（setGroupMembershipParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHANDLE | `xsd:string` | いいえ | グループメンバーシップを設定するユーザーへのハンドル。 |
| companyHandle | `xsd:string` | いいえ | 会社のハンドル。 |
| groupHandleArray | `types:HandleArray` | はい | ユーザーが属するグループへのハンドルの配列。 |

**出力（setGroupMembershipReturn）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-67b86d259df24938896fe19061845811}

このコードサンプルは、ユーザーをグループのメンバーにします。 グループハンドル配列を使用して、複数のグループにユーザーを追加します。

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
