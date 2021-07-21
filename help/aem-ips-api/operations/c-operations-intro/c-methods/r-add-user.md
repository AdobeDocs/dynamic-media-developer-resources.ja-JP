---
description: ユーザーアカウントを作成し、そのアカウントを1つ以上の会社に追加します。
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 12%

---

# addUser{#adduser}

ユーザーアカウントを作成し、そのアカウントを1つ以上の会社に追加します。

ユーザーを複数の会社に追加する場合、`companyHandleArray`で会社が取り扱う会社を指定します。 この操作は、追加したユーザーにハンドルを返します。

## 許可されたユーザーの種類 {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-40390a512e314b8d80ecffbb7729f6fb}

**入力(addUserParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`firstName`*` | `xsd:string` | はい | ユーザーの名。 |
| `*`lastName`*` | `xsd:string` | はい | ユーザーの姓。 |
| `*`電子メール`*` | `xsd:string` | はい | ユーザーの電子メールアドレス。 |
| `*`defaultRole`*` | `xsd:string` | はい | 所属する各会社のユーザーの役割を設定します。 ただし、`IpsAdmin`の役割は、他の会社ごとの設定よりも優先されます。 |
| `*`パスワード`*` | `xsd:string` | はい | ユーザーのパスワードを設定します |
| `*`passwordExpires`*` | `xsd:dateTime` | いいえ | パスワードの有効期限を設定します。 リクエストを渡す際にタイムゾーンを指定します。 タイムゾーンは中央時間に調整されます。 |
| `*`isValid`*` | `xsd:boolean` | はい | ユーザーが有効かどうかを判断します。 |
| `*`membershipArray`*` | `xsd:CompanyMembershipUpdateArray` | はい | 会社が処理する配列。 |

**出力(addUserParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| `*`userHandle`*` | `xsd:string` | はい | ユーザーへのハンドル。 |

## 例 {#section-2547cef622734b71919eef849960b5cb}

IPS APIは、新しいユーザーを指定するユーザーハンドル要素を返します。

**リクエスト**

```java
<ns1:addUserParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:firstName>Joe</ns1:firstName>
   <ns1:lastName>User</ns1:lastName>
   <ns1:email>juser@adobe.com</ns1:email>
   <ns1:defaultRole>TrialSiteUser</ns1:role>
   <ns1:password>passw0rd</ns1:password>
   <ns1:isValid>true</ns1:isValid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:addUserParam>
```

**応答**

```java
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```
