---
description: 1 つ以上の会社からユーザーを削除します。
solution: Experience Manager
title: removeCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1cb9a286-48a0-4542-a80a-c97fd973474e
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 12%

---

# removeCompanyMembership{#removecompanymembership}

1 つ以上の会社からユーザーを削除します。

構文

## 認証済みユーザータイプ {#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-6dfce5e44d8a4799afd0c231a0b10463}

**入力 (removeCompanyMembershipParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHandle | `xsd:string` | いいえ | 削除するメンバーシップを持つユーザーへのハンドル。 |
| companyHandleArray | `types:HandleArray` | はい | ユーザーを削除する会社へのハンドル。 |

**出力 (removeCompanyMembershipReturn)**

IPS API はこの操作に対する応答を返しません。

## 例 {#section-6b7903195e8647a1bd0502f87387ca62}

このコード例では、会社からユーザーを削除します。 会社ハンドル配列で指定された会社からすべてのユーザーを削除するには、オプションのユーザーハンドルを省略します。

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
