---
description: 特定の会社に属するユーザーのグループメンバーシップを設定します。
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 9%

---

# setGroupMembers{#setgroupmembers}

特定の会社に属するユーザーのグループメンバーシップを設定します。

この操作を実行する権限を持っていない場合、この操作では認証エラーがスローされます。 また、ユーザーハンドル配列内のユーザーのいずれかが、会社ハンドル内で指定された会社に属していない場合も、これは true です。

## 認証済みユーザータイプ {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-6a18562fc8e942af94be10bbb8c51151}

**入力 (setGroupMembersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| companyHandle | `xsd:string` | はい | 会社の取り扱い。 |
| groupHandle | `xsd:string` | はい | グループハンドル。 |
| userHandleArray | `types:HandleArray` | はい | グループメンバーシップを設定するユーザーのハンドルの配列。 |

**出力 (setGroupMembesReturn)**

IPS API はこの操作に対する応答を返しません。

## 例 {#section-9c528c3f44a141ce9eaddf634f26c487}

このコードのサンプルは、1 人のユーザーのグループメンバーシップを設定します。

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
