---
description: 1つ以上の会社でユーザーのメンバーシップを設定します。
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 14%

---

# setCompanyMembership{#setcompanymembership}

1つ以上の会社でユーザーのメンバーシップを設定します。

構文

## 許可されたユーザーの種類 {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-3930dc6a016140178631083563598104}

**入力(setCompanyMembershipParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:sting` | いいえ | ユーザーハンドル。 |
| `*`membershipArray`*` | `types:CompanyMembershipUpdateArray` | はい | 会社の配列。 |

**出力(setCompanyMembershipParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-862c0cc32ce0407ab248028e690a8386}

このコードサンプルは、ユーザーを会社に追加します。 必要に応じて、会社内の複数の会社がアレイを処理するように指定します。

**リクエスト**

```java
<ns1:setCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>137</ns1:items>
   </ns1:companyHandleArray>
</ns1:setCompanyMembershipParam>
```

**応答**

なし
