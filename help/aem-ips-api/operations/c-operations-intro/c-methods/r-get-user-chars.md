---
description: 特定のフィールドで使用されている文字のリストを取得します。
seo-description: 特定のフィールドで使用されている文字のリストを取得します。
seo-title: getUserChars
solution: Experience Manager
title: getUserChars
topic: Scene7 Image Production System API
uuid: c9fa7826-5174-4298-99e6-a0627e432567
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 11%

---


# getUserChars{#getuserchars}

特定のフィールドで使用されている文字のリストを取得します。

構文

## 認証済みユーザータイプ{#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメータ {#section-93107d87f1b24fc8ad276dfee5e30b63}

**入力(getUserCharsParam)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`charField`*` | `xsd:string` | はい | 検索するごみ箱の状態を指定します。 |
| ` *`includeInactive`*` | `xsd:boolean` | はい | 非アクティブなユーザーを含めるか、除外します。 IPS以外の管理者ユーザは、API呼び出しを行う権限を持つ少なくとも1人の会社のアクティブメンバである必要があります。 ユーザーがアクティブな会社メンバーシップを持っていない場合は、認証エラーが返されます。 |
| ` *`includInvalid`*` | `xsd:boolean` | いいえ | 無効なユーザーを含めるか除外します。 |
| ` *`companyHandleArray`*` | `types:HandleArray` | いいえ | 会社に基づいて結果をフィルターします。 |
| ` *`groupHandleArray`*` | `types:HandleArray` | いいえ | フィルターは、グループに基づいて結果を返します。 |
| ` *`userRoleArray`*` | `types:StringArray` | いいえ | フィルターの役割に基づく結果です。 |
| ` *`numChars`*` | `xsd:int` | いいえ | >1文字を有効にします。 |

**出力(getUserCharsReturn)**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| ` *`userCharsArray`*` | `types:StringArray` | はい | 文字プリフィックスの配列。 |

## 例 {#section-3702f165e8b041139a6144f4a76ca25f}

次のコードサンプルが返します。

* 特定の会社のユーザーの姓の最初の文字。
* グループのセット。
* ユーザーの役割のセット。

User Char Filter Fields文字列定数は、返されるユーザー文字の種類を決定します。

**リクエスト**

```java
<ns1:getUserCharsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:charField>LastName</ns1:charField>
   <ns1:includeInvalid>false</ns1:includeInvalid>
   <ns1:companyHandleArray>
      <ns1:items>47</ns1:items>
   </ns1:companyHandleArray>
</ns1:getUserCharsParam>
```

**応答**

```java
<getUserCharsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <userCharsArray>
      <items>b</items>
      <items>c</items>
      <items>d</items>
   </userCharsArray>
</getUserCharsReturn>
```

