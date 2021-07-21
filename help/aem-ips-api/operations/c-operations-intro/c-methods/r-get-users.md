---
description: 会社、グループ、およびユーザーの役割のハンドルで指定されたユーザーの配列を取得します。 この操作では、返されたユーザーを並べ替え、文字でフィルターできます。
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 10%

---

# getUsers{#getusers}

会社、グループ、およびユーザーの役割のハンドルで指定されたユーザーの配列を取得します。 この操作では、返されたユーザーを並べ替え、文字でフィルターできます。

## 許可されたユーザーの種類 {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`includeInactive`*` | `xsd:boolean` | いいえ | 非アクティブなユーザーを含めるか除外します。 IPS以外の管理者ユーザーは、API呼び出しをおこなう権限を持つ1社以上のアクティブなメンバーである必要があります。 ユーザーがアクティブな会社メンバーシップを持っていない場合、承認エラーが返されます。 |
| `*`includeInvalid`*` | `xsd:boolean` | いいえ | 無効なユーザーを含めるか除外するかを指定します。 |
| `*`companyHandleArray`*` | `types:HandleArray` | いいえ | 会社で結果をフィルターします。 |
| `*`groupHandleArray`*` | `types:HandleArray` | いいえ | 結果をグループでフィルターします。 |
| `*`userRoleArray`*` | `types:StringArray` | いいえ | ユーザーの役割で結果をフィルターします。 |
| `*`charFilterField`*` | `xsd:string` | いいえ | フィールドの文字列プレフィックスで結果をフィルターします([!DNL Trash State).] |
| `*`charFilter`*` | `xsd:string` | いいえ | 特定の文字で結果をフィルターします。 |
| `*`sortBy`*` | `xsd:string` | いいえ | ユーザーによる並べ替えフィールドの選択。 |
| `*`recordsPerPage`*` | `xsd:int` | いいえ | 1ページあたりの指定されたレコード数を返します。 |
| `*`resultsPage`*` | `xsd:int` | いいえ | 結果ページ |

**出力(getUsersReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | はい | ユーザーの配列。 |

## 例 {#section-bc43a5dd7b4c4f048d25fc881554dab2}

このコードサンプルは、いくつかのオプションパラメーターのユーザーの配列を返します。 ユーザーの役割、ユーザー文字フィルターフィールド、ユーザーの並べ替えフィールドは、特定の文字列定数を使用して決定されます。

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
