---
description: 1 つ以上の会社のユーザーのメンバーシップを設定します。
solution: Experience Manager
title: setCompanyMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 11%

---

# setCompanyMembers{#setcompanymembership}

1 つ以上の会社のユーザーのメンバーシップを設定します。

構文

## 許可されているユーザータイプ {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-3930dc6a016140178631083563598104}

**入力（setCompanyMembershipParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHandle | `xsd:sting` | いいえ | ユーザーハンドル。 |
| membershipArray | `types:CompanyMembershipUpdateArray` | はい | 会社の配列。 |

**出力（setCompanyMembershipParam）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-862c0cc32ce0407ab248028e690a8386}

このコードサンプルでは、会社にユーザーを追加します。 必要に応じて、会社ハンドル配列に複数の会社を指定します。

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
