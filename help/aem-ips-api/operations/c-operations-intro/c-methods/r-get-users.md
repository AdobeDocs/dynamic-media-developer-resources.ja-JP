---
description: 会社、グループ、ユーザーのロール ハンドルで指定されたユーザーの配列を取得します。 この操作を使用すると、返されたユーザーを並べ替え、文字別にフィルターできます。
solution: Experience Manager
title: getUsers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dfdcbcdd-232f-4c73-9520-c7c958eedf54
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 9%

---

# getUsers{#getusers}

会社、グループ、ユーザーのロール ハンドルで指定されたユーザーの配列を取得します。 この操作を使用すると、返されたユーザーを並べ替え、文字別にフィルターできます。

## 許可されているユーザータイプ {#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| includeInactive | `xsd:boolean` | いいえ | 非アクティブユーザーを含めるか除外します。 IPS 以外の管理者ユーザーは、API 呼び出しを行う権限を付与される少なくとも 1 つの会社のアクティブメンバーである必要があります。 ユーザーにアクティブな会社のメンバーシップがない場合、認証エラーが返されます。 |
| includeInvalid | `xsd:boolean` | いいえ | 無効なユーザーを含めたり除外したりできます。 |
| companyHandleArray | `types:HandleArray` | いいえ | 結果を会社でフィルタリングします。 |
| groupHandleArray | `types:HandleArray` | いいえ | 結果をグループでフィルタリングします。 |
| userRoleArray | `types:StringArray` | いいえ | ユーザーロール別に結果をフィルターします。 |
| charFilterField | `xsd:string` | いいえ | フィールドの文字列プレフィックスによる結果のフィルタリング（[!DNL Trash State).] を参照） |
| charFilter | `xsd:string` | いいえ | 特定の文字で結果をフィルタリングします。 |
| sortBy | `xsd:string` | いいえ | ユーザー並べ替えフィールドの選択。 |
| recordsPerPage | `xsd:int` | いいえ | ページごとに指定されたレコード数を返します。 |
| resultsPage | `xsd:int` | いいえ | 結果ページ。 |

**出力（getUsersReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userArray | `types:UserArray` | はい | ユーザーの配列。 |

## 例 {#section-bc43a5dd7b4c4f048d25fc881554dab2}

このコードサンプルでは、複数のオプションパラメーターに対するユーザーの配列を返します。 ユーザーの役割、ユーザー文字フィルターフィールド、ユーザーの並べ替えフィールドは、特定の文字列定数を使用して決定されます。

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
