---
description: 会社、グループ、およびユーザの役割のハンドルで指定されたユーザの配列を取得します。 この操作では、返されたユーザーを並べ替え、文字でフィルターできます。
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 10%

---

# getUsers{#getusers}

会社、グループ、およびユーザの役割のハンドルで指定されたユーザの配列を取得します。 この操作では、返されたユーザーを並べ替え、文字でフィルターできます。

## 認証済みユーザータイプ {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| includeInactive | `xsd:boolean` | いいえ | 非アクティブなユーザーを含めるか除外します。 IPS 管理者以外のユーザーは、API 呼び出しをおこなう権限を持つ 1 つ以上の会社のアクティブなメンバーである必要があります。 ユーザーがアクティブな会社メンバーシップを持っていない場合、認証エラーが返されます。 |
| includeInvalid | `xsd:boolean` | いいえ | 無効なユーザーを含める/除外できます。 |
| companyHandleArray | `types:HandleArray` | いいえ | 結果を会社でフィルタリングします。 |
| groupHandleArray | `types:HandleArray` | いいえ | 結果をグループでフィルターします。 |
| userRoleArray | `types:StringArray` | いいえ | ユーザーの役割で結果をフィルタリングします。 |
| charFilterField | `xsd:string` | いいえ | フィールドの文字列プレフィックスで結果をフィルタリングします ( [!DNL Trash State).] |
| charFilter | `xsd:string` | いいえ | 特定の文字で結果をフィルタリングします。 |
| sortBy | `xsd:string` | いいえ | ユーザーによる並べ替えフィールドの選択。 |
| recordsPerPage | `xsd:int` | いいえ | 1 ページあたりの指定されたレコード数を返します。 |
| resultsPage | `xsd:int` | いいえ | 結果ページ。 |

**出力 (getUsersReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userArray | `types:UserArray` | はい | ユーザーの配列。 |

## 例 {#section-bc43a5dd7b4c4f048d25fc881554dab2}

このコードサンプルは、複数のオプションパラメーターのユーザーの配列を返します。 ユーザーの役割、ユーザーの文字フィルターフィールド、ユーザーの並べ替えフィールドは、特定の文字列定数を使用して決定されます。

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
