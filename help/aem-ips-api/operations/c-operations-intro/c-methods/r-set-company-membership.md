---
description: 1つ以上の会社のメンバーシップを設定します。
seo-description: 1つ以上の会社のメンバーシップを設定します。
seo-title: setCompanyMembership
solution: Experience Manager
title: setCompanyMembership
topic: Scene7 Image Production System API
uuid: 34c9d457-bc2e-4186-8a8f-50388410640a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 13%

---


# setCompanyMembership{#setcompanymembership}

1つ以上の会社のメンバーシップを設定します。

構文

## 認証済みユーザータイプ{#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-3930dc6a016140178631083563598104}

**入力(setCompanyMembershipParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:sting` | いいえ | ユーザーハンドル。 |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | はい | 会社の配列。 |

**Output (setCompanyMembershipParam)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-862c0cc32ce0407ab248028e690a8386}

このコードの例では、会社にユーザーを追加します。 必要に応じて、会社ハンドル配列に複数の会社を指定します。

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
