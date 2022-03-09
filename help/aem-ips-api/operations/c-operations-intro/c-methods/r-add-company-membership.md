---
description: 1 つ以上の会社にユーザーを追加します。
solution: Experience Manager
title: addCompanyMembership
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6efef4fb-f2e5-4c41-b739-a36ac2f17884
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 14%

---

# addCompanyMembership{#addcompanymembership}

1 つ以上の会社にユーザーを追加します。

構文

## 認証済みユーザータイプ {#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**入力 (addCompanyMembershipParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHandle | `xsd:string` | いいえ | メンバーシップを追加するユーザーのハンドル。 |
| membershipArray | `types:CompanyMembershipUpdateArray` | はい | ユーザーを追加する会社の配列。 |

**出力 (addCompanyMembershipReturn)**

IPS API はこの操作に対する応答を返しません。

## 例 {#section-5469f88bac7047cca131faa6b021e437}

この例では、companyHandleArray を使用して、1 つの会社にユーザーを追加します。

**リクエスト**

```javascript {.line-numbers}
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**応答**

なし
