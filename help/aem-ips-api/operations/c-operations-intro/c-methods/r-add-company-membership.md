---
description: 1つ以上の会社にユーザーを追加します。
seo-description: 1つ以上の会社にユーザーを追加します。
seo-title: addCompanyMembership
solution: Experience Manager
title: addCompanyMembership
topic: Scene7 Image Production System API
uuid: be55041c-fc4e-46e8-bd2c-81b5931406f5
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 13%

---


# addCompanyMembership{#addcompanymembership}

1つ以上の会社にユーザーを追加します。

構文

## 認証済みユーザータイプ{#section-ae926c7672984be79f6102748accab72}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-0e925b91d63e48aa91f0b0014e6a0cab}

**入力(addCompanyMembershipParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`userHandle`*` | `xsd:string` | いいえ | メンバーシップを追加するユーザーのハンドルです。 |
| ` *`membershipArray`*` | `types:CompanyMembershipUpdateArray` | はい | ユーザーを追加する会社の配列。 |

**Output (addCompanyMembershipReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-5469f88bac7047cca131faa6b021e437}

この例では、` *`companyHandleArray`*`を使用して、1人の会社に1人のユーザを追加しています。

**リクエスト**

```java
<ns1:addCompanyMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>621|jduvar@adobe.com</ns1:userHandle>
   <ns1:companyHandleArray>
      </ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addCompanyMembershipParam>
```

**応答**

なし
