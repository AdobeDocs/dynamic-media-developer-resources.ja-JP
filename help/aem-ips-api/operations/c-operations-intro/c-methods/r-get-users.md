---
description: 会社、グループ、ユーザーの役割ハンドルで指定されたユーザーの配列を取得します。 この操作では、返されたユーザーを並べ替え、文字でフィルタリングできます。
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
TQID: 'https://experienceleague.adobe.com/17FQLNVfRg84FeVetVfuTWoLRMf8ugBwXBi2CpmLZfI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: ba0745708154402d9b6c7ebf0554deb366dde11b
workflow-type: tm+mt
source-wordcount: 209
ht-degree: 9%

---

# getUsers{#getusers}

会社、グループ、ユーザーの役割ハンドルで指定されたユーザーの配列を取得します。 この操作では、返されたユーザーを並べ替え、文字でフィルタリングできます。

## 承認済みユーザータイプ {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| includeInactive | `xsd:boolean` | いいえ | 非アクティブユーザーを含めるか除外します。 非IPS管理者ユーザーは、API呼び出しを行う権限を持つ少なくとも1つの企業のアクティブなメンバーである必要があります。 ユーザーにアクティブな会社メンバーシップがない場合、認証エラーが返されます。 |
| includeInvalid | `xsd:boolean` | いいえ | 無効なユーザーを含める/除外できます。 |
| companyHandleArray | `types:HandleArray` | いいえ | 企業ごとに結果をフィルタリング。 |
| groupHandleArray | `types:HandleArray` | いいえ | グループ別に結果をフィルタリング。 |
| userRoleArray | `types:StringArray` | いいえ | ユーザーの役割ごとに結果をフィルタリング。 |
| charFilterField | `xsd:string` | いいえ | フィールドの文字列プレフィックスで結果をフィルタリングします（[!DNL Trash State).]を参照） |
| charFilter | `xsd:string` | いいえ | 特定の文字で結果をフィルタリングします。 |
| sortBy | `xsd:string` | いいえ | ユーザーソートフィールドの選択。 |
| recordsPerPage | `xsd:int` | いいえ | ページあたりの指定されたレコード数を返します。 |
| resultsPage | `xsd:int` | いいえ | 結果ページ： |

**出力（getUsersReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userArray | `types:UserArray` | はい | ユーザーの配列。 |

## 例 {#section-bc43a5dd7b4c4f048d25fc881554dab2}

このコードサンプルは、オプションのパラメーターを指定して、ユーザーの配列を返します。 ユーザーロール、ユーザー文字フィルターフィールド、ユーザーソートフィールドは、特定の文字列定数を使用して決定されます。

**リクエスト**

```java
<ns1:getUsersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
   <ns1:userRoleArray>
      <ns1:items>IpsAdmin</ns1:items>
   </ns1:userRoleArray>
   <ns1:sortBy>LastName</ns1:sortBy>
</ns1:getUsersParam>
```

**応答**

```java
<getUsersReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userArray>
      <items>
         <userHandle>70|kmagnusson@adobe.com</userHandle>
         <firstName>Kris</firstName>
         <lastName>Magnusson</lastName>
         <email>kmagnusson@adobe.com</email>
         <role>IpsAdmin</role>
         <isValid>true</isValid>
         <passwordExpires>2107-07-27T15:18:15.816-07:00</passwordExpires>
      </items>
      ...
   </userArray>
</getUsersReturn>
```

