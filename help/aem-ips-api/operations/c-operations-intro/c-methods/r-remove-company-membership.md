---
description: ユーザーを1つ以上の会社から削除します。
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
TQID: 'https://experienceleague.adobe.com/5jjL8MnUtL046oSej3HErZB9hrD-ueEBC5-h9vD92HM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 9%

---

# removeCompanyMembership{#removecompanymembership}

ユーザーを1つ以上の会社から削除します。

構文

## 承認済みユーザータイプ {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-6dfce5e44d8a4799afd0c231a0b10463}

**入力（removeCompanyMembershipParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHANDLE | `xsd:string` | いいえ | 削除するメンバーシップを持つユーザーへのハンドル。 |
| companyHandleArray | `types:HandleArray` | はい | ユーザーを削除する会社へのハンドル。 |

**出力（removeCompanyMembershipReturn）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-6b7903195e8647a1bd0502f87387ca62}

このコードサンプルは、企業からユーザーを削除します。 会社ハンドル配列で指定された会社からすべてのユーザーを削除するには、オプションのユーザーハンドルを省略します。

**リクエスト**

```java
<ns1:removeCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:removeCompanyMembershipParam>
```

**応答**

なし
