---
description: 特定のフィールドで使用されている文字のリストを取得します。
solution: Experience Manager
title: getUserChar
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d6b79c06-0e90-406f-bac8-3b8c2bae5480
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 10%

---

# getUserChar{#getuserchars}

特定のフィールドで使用されている文字のリストを取得します。

構文

## 許可されているユーザータイプ {#section-7023871be4d2442daf51ff060ca06d9a}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## パラメーター {#section-93107d87f1b24fc8ad276dfee5e30b63}

**入力（getUserCharsParam）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| charField | `xsd:string` | はい | 検索するごみ箱の状態を決定します。 |
| includeInactive | `xsd:boolean` | はい | 非アクティブユーザーを含めるか除外します。 IPS 以外の管理者ユーザーは、API 呼び出しを行う権限を付与される少なくとも 1 つの会社のアクティブメンバーである必要があります。 ユーザーにアクティブな会社のメンバーシップがない場合、認証エラーが返されます。 |
| includInvalid | `xsd:boolean` | いいえ | 無効なユーザーを含めるか除外します。 |
| companyHandleArray | `types:HandleArray` | いいえ | 会社に基づいて結果をフィルターします。 |
| groupHandleArray | `types:HandleArray` | いいえ | グループに基づいて結果をフィルタリングします。 |
| userRoleArray | `types:StringArray` | いいえ | ユーザーロールに基づいて結果をフィルターします。 |
| numChars | `xsd:int` | いいえ | >1 文字を有効にします。 |

**出力（getUserCharsReturn）**

| 名前 | 種類 | 必須 | 説明 |
|---|---|---|---|
| userCharsArray | `types:StringArray` | はい | 文字プレフィックスの配列。 |

## 例 {#section-3702f165e8b041139a6144f4a76ca25f}

このコードサンプルでは、次の情報が返されます。

* 特定の会社のユーザーの姓の先頭文字。
* グループのセット。
* ユーザーの役割のセット。

ユーザー文字フィルターフィールドの文字列定数は、返されるユーザー文字の種類を決定します。

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
