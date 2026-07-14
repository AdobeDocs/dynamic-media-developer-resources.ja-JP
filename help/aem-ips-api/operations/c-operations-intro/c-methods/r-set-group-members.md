---
description: 特定の会社に属するユーザーのグループメンバーシップを設定します。
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
TQID: 'https://experienceleague.adobe.com/9gCJ-UKUNZI3AbQ0LFkxNUSS-w7bnG0FQE8SQeM2MMQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 6762cee83f1b7c970ed6353450c2ae6c602e7f3a
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 7%

---

# setGroupMembers{#setgroupmembers}

特定の会社に属するユーザーのグループメンバーシップを設定します。

この操作を実行する権限がない場合、この操作は認証失敗をスローします。 これは、ユーザーハンドル配列内のユーザーのいずれかが、会社ハンドルで指定された会社に属していない場合にも当てはまります。

## 承認済みユーザータイプ {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-6a18562fc8e942af94be10bbb8c51151}

**入力（setGroupMembersParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社のハンドル。 |
| groupHandle | `xsd:string` | はい | グループハンドル： |
| userHandleArray | `types:HandleArray` | はい | グループメンバーシップを設定するユーザーのハンドルの配列。 |

**出力（setGroupMembesReturn）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-9c528c3f44a141ce9eaddf634f26c487}

このコードのサンプルでは、1人のユーザーのグループ メンバーシップを設定します。

**リクエスト**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**応答**

なし

