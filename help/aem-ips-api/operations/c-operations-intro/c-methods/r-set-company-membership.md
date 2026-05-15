---
description: 1つ以上の会社でユーザーのメンバーシップを設定します。
solution: Experience Manager
title: setCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 43144c75-1d83-4e1d-8319-c3275d349a2f
TQID: 'https://experienceleague.adobe.com/Nb9XjcAX4NMyne48B9QoVqlhUnhCE5ufIHILopUeAf0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 76
ht-degree: 11%

---

# setCompanyMembership{#setcompanymembership}

1つ以上の会社でユーザーのメンバーシップを設定します。

構文

## 承認済みユーザータイプ {#section-0cbcc78cfee64c2baf66f29cce6d0a65}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-3930dc6a016140178631083563598104}

**入力（setCompanyMembershipParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHANDLE | `xsd:sting` | いいえ | ユーザーハンドル： |
| membershipArray | `types:CompanyMembershipUpdateArray` | はい | 企業の数々。 |

**出力（setCompanyMembershipParam）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-862c0cc32ce0407ab248028e690a8386}

このコードサンプルは、ユーザーを会社に追加します。 必要に応じて、会社ハンドル配列に複数の会社を指定します。

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
