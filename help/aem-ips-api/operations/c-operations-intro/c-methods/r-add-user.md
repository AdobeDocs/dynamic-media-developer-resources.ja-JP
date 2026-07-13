---
description: ユーザーアカウントを作成し、そのアカウントを1つ以上の企業に追加します。
solution: Experience Manager
title: addUser
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: aed39e73-f528-4c26-8f62-c3d796e9101a
TQID: 'https://experienceleague.adobe.com/dR1bVB3TeSd9qnnVPrp0YIg3-kS51rPHnVWVVrhZt8s'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4185012f22b173b569d11ea4d350763a82f98710
workflow-type: tm+mt
source-wordcount: 177
ht-degree: 11%

---

# addUser{#adduser}

ユーザーアカウントを作成し、そのアカウントを1つ以上の企業に追加します。

ユーザーを複数の会社に追加する場合は、それらの会社を`companyHandleArray`の会社ハンドルで指定します。 この操作は、追加したユーザーにハンドルを返します。

## 承認済みユーザータイプ {#section-126ad42f844444fea11ecf8ad01fe1ec}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-40390a512e314b8d80ecffbb7729f6fb}

**入力（addUserParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| firstName | `xsd:string` | はい | ユーザーの名前。 |
| lastName | `xsd:string` | はい | ユーザーの姓。 |
| 電子メール | `xsd:string` | はい | ユーザーのメールアドレス。 |
| defaultRole | `xsd:string` | はい | ユーザーが属する各会社におけるユーザーの役割を設定します。 ただし、`IpsAdmin`の役割は、会社ごとの他の設定よりも優先されます。 |
| パスワード | `xsd:string` | はい | ユーザーのパスワードを設定します |
| passwordExpires | `xsd:dateTime` | いいえ | パスワードの有効期限を設定します。 リクエストを渡す際にタイムゾーンを指定します。 タイムゾーンは中央の時間に調整されます。 |
| isValid | `xsd:boolean` | はい | ユーザーが有効かどうかを判断します。 |
| membershipArray | `xsd:CompanyMembershipUpdateArray` | はい | 企業が処理する一連の処理です。 |

**出力（addUserParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userHANDLE | `xsd:string` | はい | ユーザーへのハンドル。 |

## 例 {#section-2547cef622734b71919eef849960b5cb}

IPS APIは、新しいユーザーを指定するユーザーハンドル要素を返します。

**リクエスト**

```java {.line-numbers}
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

```java {.line-numbers}
<ns1:addUserReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:userHandle>525s|juser@scene7.com</ns1:userHandle>
</ns1:addUserReturn>
```

