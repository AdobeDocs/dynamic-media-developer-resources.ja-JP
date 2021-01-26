---
description: 会社、グループ、およびユーザーの役割ハンドルで指定されたユーザーの配列を取得します。 この操作により、返されたユーザーを並べ替えたり、文字でフィルターしたりできます。
seo-description: 会社、グループ、およびユーザーの役割ハンドルで指定されたユーザーの配列を取得します。 この操作により、返されたユーザーを並べ替えたり、文字でフィルターしたりできます。
seo-title: getUsers
solution: Experience Manager
title: getUsers
topic: Dynamic Media Image Production System API
uuid: f16ccd1b-0f00-4d9a-b6e1-6abc3bde1af9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 9%

---


# getUsers{#getusers}

会社、グループ、およびユーザーの役割ハンドルで指定されたユーザーの配列を取得します。 この操作により、返されたユーザーを並べ替えたり、文字でフィルターしたりできます。

## 認証済みユーザータイプ{#section-6a8f23cc6b22442d8776f701016971ed}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`


| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`includeInactive`*` | `xsd:boolean` | いいえ | 非アクティブなユーザーを含めるか、除外します。 IPS以外の管理者ユーザは、API呼び出しを行う権限を持つ少なくとも1人の会社のアクティブメンバである必要があります。 ユーザーがアクティブな会社メンバーシップを持っていない場合は、認証エラーが返されます。 |
| `*`includeInvalid`*` | `xsd:boolean` | いいえ | 無効なユーザーを含める/除外できます。 |
| `*`companyHandleArray`*` | `types:HandleArray` | いいえ | 会社で結果をフィルターします。 |
| `*`groupHandleArray`*` | `types:HandleArray` | いいえ | 結果をグループでフィルターします。 |
| `*`userRoleArray`*` | `types:StringArray` | いいえ | ユーザーの役割で結果をフィルターします。 |
| `*`charFilterField`*` | `xsd:string` | いいえ | フィールドの文字列プレフィックスで結果をフィルタします（[!DNL Trash State).]を参照） |
| `*`charFilter`*` | `xsd:string` | いいえ | 特定の文字で結果をフィルタリングします。 |
| `*`sortBy`*` | `xsd:string` | いいえ | ユーザーによる並べ替えフィールドの選択 |
| `*`recordsPerPage`*` | `xsd:int` | いいえ | 1ページに指定した数のレコードを返します。 |
| `*`resultsPage`*` | `xsd:int` | いいえ | 結果ページ |

**Output (getUsersReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userArray`*` | `types:UserArray` | はい | 一連のユーザー。 |

## 例 {#section-bc43a5dd7b4c4f048d25fc881554dab2}

次のコードのサンプルを使用すると、いくつかのオプションのパラメーターに対してユーザーの配列を返すことができます。 ユーザーの役割、ユーザーの文字フィルターフィールド、ユーザーの並べ替えフィールドは、特定の文字列定数を使用して決定されます。

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

