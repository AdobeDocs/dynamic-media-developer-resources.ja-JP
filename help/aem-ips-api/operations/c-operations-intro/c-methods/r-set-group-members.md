---
description: 特定の会社に属するユーザーのグループメンバーシップを設定します。
seo-description: 特定の会社に属するユーザーのグループメンバーシップを設定します。
seo-title: setGroupMembers
solution: Experience Manager
title: setGroupMembers
topic: Scene7 Image Production System API
uuid: fe6585ef-a4b3-4b3c-95d0-624017650497
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setGroupMembers{#setgroupmembers}

特定の会社に属するユーザーのグループメンバーシップを設定します。

この操作を実行する権限がない場合、操作によって認証エラーがスローされます。 これは、ユーザハンドル配列内のユーザの中に、会社のハンドルで指定された会社に属していないユーザがいる場合にも当てはまります。

## 認証されたユーザータイプ {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-6a18562fc8e942af94be10bbb8c51151}

**入力(setGroupMembersParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | はい | 会社の担当。 |
| ` *`groupHandle`*` | `xsd:string` | はい | グループハンドル。 |
| ` *`userHandleArray`*` | `types:HandleArray` | はい | グループメンバーシップを設定するユーザーのハンドルの配列。 |

**出力(setGroupMembesReturn)**

IPS APIはこの操作に対する応答を返しません。

## 例 {#section-9c528c3f44a141ce9eaddf634f26c487}

このコードのサンプルでは、1人のユーザーのグループメンバーシップを設定します。

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
