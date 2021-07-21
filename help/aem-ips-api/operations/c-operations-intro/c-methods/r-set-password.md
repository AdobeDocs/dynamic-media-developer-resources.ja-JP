---
description: ユーザーハンドルを指定するかどうかに応じて、特定のユーザーまたはデフォルトのユーザーのパスワードを特定の値に設定します。
solution: Experience Manager
title: setPassword
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin
exl-id: e8d95b55-0a97-4887-b711-7be99833c389
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 5%

---

# setPassword{#setpassword}

ユーザーハンドルを指定するかどうかに応じて、特定のユーザーまたはデフォルトのユーザーのパスワードを特定の値に設定します。

パスワードの有効期限はオプションです。 省略した場合、パスワードの有効期限は無期限になります。

## 認証済みユーザータイプ {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>** 他のユーザー `IpsAdmin` に対してsetPassword呼び出しを実行する権限があるのは、ユーザータイプのみです。

* `IpsAdmin`
* `IpsCompanyAdmin`
* `IpsUser`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* `ImagePortalUser`

## パラメータ {#section-0531294341f7483d89dacaa393dd659a}

**入力(setPasswordParam)**

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
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> userHandle  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>ユーザーハンドル。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> パスワード  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>パスワード. </p> <p>選択したパスワードに対して、次の要件が適用されます。 </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">パスワードでは大文字と小文字が区別されます。 </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">パスワードの最小長は8文字です。 </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">パスワードには、次の文字クラスの1つ以上の文字を含める必要があります。 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">小文字の英語文字。 例： <span class="codeph"> a b c d e </span>など </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">大文字の英語文字。 例えば、 <span class="codeph"> A B C D E </span>などです。 </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">数値。 例えば、 <span class="codeph"> 1 2 3 4 5 </span>などです。 </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">特殊文字。 例えば、次のいずれかを使用できます。<span class="codeph"> &amp;grave;～!@ # $ % ^ * ( ) _ + - = { } | [ ] &amp; \ :" ;' &lt; &gt; ?, . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> passwordExpires  </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime  </span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>パスワードの有効期限を決定します。 <p>注意： このフィールドのリクエストでタイムゾーンを指定します。 タイムゾーンは中央時間に調整されます。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力(setPasswordReturn)**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-23a6fbabdb3c4c3180076057e47ae567}

このコードのサンプルでは、ユーザーパスワードを作成します。 `passwordExpires`が省略されたので、パスワードの有効期限は切れません。

**リクエスト**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**応答**

なし
