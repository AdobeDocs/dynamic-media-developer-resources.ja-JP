---
description: ユーザーのグループメンバーシップを設定します。
seo-description: ユーザーのグループメンバーシップを設定します。
seo-title: setGroupMembership
solution: Experience Manager
title: setGroupMembership
topic: Scene7 Image Production System API
uuid: 3285fab0-92e4-4b88-9a3c-88cbb97d48c9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 12%

---


# setGroupMembership{#setgroupmembership}

ユーザーのグループメンバーシップを設定します。

構文

## 認証済みユーザータイプ{#section-3d6308a8a5694ed085e04d1c37982b9e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-6aeda13b26af4796aad1306ac7a9ad17}

**入力(setGroupMembershipParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | いいえ | グループメンバーシップを設定するユーザーのハンドル。 |
| ` *`companyHandle`*` | `xsd:string` | いいえ | 会社ハンドル |
| ` *`groupHandleArray`*` | `types:HandleArray` | はい | ユーザーが属するグループへのハンドルの配列。 |

**出力(setGroupMembershipReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-67b86d259df24938896fe19061845811}

このコードのサンプルを使用すると、ユーザーがグループのメンバーになります。 グループ・ハンドル配列追加を持つ複数のグループに対するユーザー

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
