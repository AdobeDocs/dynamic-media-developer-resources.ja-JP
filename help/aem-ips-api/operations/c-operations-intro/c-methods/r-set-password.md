---
description: ユーザーハンドルを指定するかどうかに応じて、特定のユーザーのパスワードまたはデフォルトユーザーのパスワードを特定の値に設定します。
solution: Experience Manager
title: setPassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e8d95b55-0a97-4887-b711-7be99833c389
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 3%

---

# setPassword{#setpassword}

ユーザーハンドルを指定するかどうかに応じて、特定のユーザーのパスワードまたはデフォルトユーザーのパスワードを特定の値に設定します。

パスワードの有効期限はオプションです。 省略すると、パスワードの有効期限は設定されません。

## 許可されているユーザータイプ {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*のみ*`IpsAdmin` ユーザータイプは、他のユーザーに対して setPassword 呼び出しを実行することを許可されています。

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## パラメーター {#section-0531294341f7483d89dacaa393dd659a}

**入力（setPasswordParam）**

<table id="table_BF54512811344E0B979C5070354E8048"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名前 </p> </th> 
   <th colname="col2" class="entry"> <p>種類 </p> </th> 
   <th colname="col3" class="entry"> <p>必須 </p> </th> 
   <th colname="col4" class="entry"> <p>説明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>ユーザーハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> password </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>パスワード。 </p> <p>選択したパスワードには、次の要件が適用されます。 </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">パスワードでは大文字と小文字が区別されます。 </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">パスワードの長さは最低 8 文字です。 </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">パスワードには、次の文字クラスの 1 つ以上の文字が含まれている必要があります。 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">英語の小文字。 例：<span class="codeph"> a b c d e </span> など </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">英大文字。 例えば、<span class="codeph"> A B C D E </span> など。 </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">数値。 例えば、<span class="codeph"> 1 2 3 4 5 </span> など。 </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">特殊文字。 例えば、次のいずれかを使用できます。<span class="codeph"> &grave; ～ !@ # $ % ^ * （） _ + - = { } | [ ] &amp; \ : " ; ' &lt; &gt; ?, . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpires </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime </span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>パスワードの有効期限を決定します。 <p>メモ：このフィールドに対するリクエストのタイムゾーンを指定します。 タイムゾーンは中部標準時に調整されます。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力（setPasswordReturn）**

IPS API は、この操作に対して応答を返しません。

## 例 {#section-23a6fbabdb3c4c3180076057e47ae567}

このコードサンプルでは、ユーザーパスワードを作成します。 パスワードが省略されたので、有効期限 `passwordExpires` 設定されません。

**リクエスト**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**応答**

なし
