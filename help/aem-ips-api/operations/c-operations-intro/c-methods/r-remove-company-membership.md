---
description: 1つ以上の会社からユーザーを削除します。
seo-description: 1つ以上の会社からユーザーを削除します。
seo-title: removeCompanyMembership
solution: Experience Manager
title: removeCompanyMembership
topic: Dynamic Media Image Production System API
uuid: af57fde0-2297-41da-87bf-f063fc313264
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 11%

---


# removeCompanyMembership{#removecompanymembership}

1つ以上の会社からユーザーを削除します。

構文

## 認証済みユーザータイプ{#section-e9a16c8a7d8d4845989a1488c9ca9c98}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-6dfce5e44d8a4799afd0c231a0b10463}

**入力(removeCompanyMembershipParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | いいえ | 削除するメンバーシップを持つユーザーへのハンドル。 |
| `*`companyHandleArray`*` | `types:HandleArray` | はい | ユーザーを削除する会社のハンドル。 |

**出力(removeCompanyMembershipReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-6b7903195e8647a1bd0502f87387ca62}

このコードの例では、会社からユーザーを削除します。 会社ハンドルの配列で指定された会社からすべてのユーザーを削除するには、オプションのユーザーハンドルを省略します。

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
