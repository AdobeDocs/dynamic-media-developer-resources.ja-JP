---
description: ユーザーハンドルを指定するかどうかに応じて、特定のユーザーまたはデフォルトユーザーのパスワードを特定の値に設定します。
solution: Experience Manager
title: setPassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e8d95b55-0a97-4887-b711-7be99833c389
TQID: 'https://experienceleague.adobe.com/01-S0tkyxnXa6YT4Wch4SB5kPAcTo-ImUhN4uNUY3ks'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 230
ht-degree: 3%

---

# setPassword{#setpassword}

ユーザーハンドルを指定するかどうかに応じて、特定のユーザーまたはデフォルトユーザーのパスワードを特定の値に設定します。

パスワードの有効期限はオプションです。 省略した場合、パスワードは期限切れになりません。

## 承認済みユーザータイプ {#section-39ae61d78cab4492a6efc1fc0d2f06c4}

>[!NOTE]
>
>*ユーザータイプ `IpsAdmin`の*&#x200B;のみが、他のユーザーに対してsetPassword呼び出しを実行する権限を持っています。

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
   <td colname="col4"> <p>ユーザーハンドル： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> パスワード </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string </span> </p> </td> 
   <td colname="col3"> <p>はい </p> </td> 
   <td colname="col4"> <p>パスワード。 </p> <p>選択したパスワードには、次の要件が適用されます。 </p> <p> 
     <ul id="ul_E5BE3621127C476788412174584075B3"> 
      <li id="li_0132852AFD774659A0224C450F19418C">パスワードでは大文字と小文字が区別されます。 </li> 
      <li id="li_71224B3A89C8461AB689BAD383EC8CEA">パスワードの最小長は8文字です。 </li> 
      <li id="li_C21B6843EA734D1ABE0580185F775408">パスワードには、次の文字クラスの1つ以上の文字を含める必要があります。 
       <ul id="ul_D5D3911AD6214035BBD2AB8350A459C7"> 
        <li id="li_6E3F084100104F2CBCF130EF8852C7B7">小文字で英字を表示します。 例：<span class="codeph"> a b c d e </span>など </li> 
        <li id="li_1FDED8D7348842BC857320D797D41217">大文字の英字。 例：<span class="codeph"> A B C D E </span>など。 </li> 
        <li id="li_C3C4D5412AA749F3B78F37B2B696CF80">データを。 例えば、<span class="codeph"> 1 2 3 4 5 </span>などがあります。 </li> 
        <li id="li_2730798F26E74B878BEDE510CD06D8DD">特殊記号の文字 例えば、次のいずれかを使用できます。<span class="codeph"> &grave; ～ ! @ # $ % ^ * ( ) _ + - = { } | [ ] &amp; \ : " ; ' &lt; &gt; ? , . / </span> </li> 
       </ul> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> パスワード有効期限</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:dateTime </span> </p> </td> 
   <td colname="col3"> <p>いいえ </p> </td> 
   <td colname="col4"> <p>パスワードの有効期限を指定します。 <p>注意：このフィールドのリクエストをタイムゾーンに指定します。 タイムゾーンは中央の時間に調整されます。 </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

**出力（setPasswordReturn）**

IPS APIは、この操作に対する応答を返しません。

## 例 {#section-23a6fbabdb3c4c3180076057e47ae567}

このコードのサンプルでは、ユーザーのパスワードを作成します。 `passwordExpires`が省略されたため、パスワードは期限切れになりません。

**リクエスト**

```java
<ns1:setPasswordParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">  
   <ns1:userHandle>3341|juser@scene7.com</ns1:userHandle> 
   <ns1:password>@Do6e$ySt3mz</ns1:password> 
</ns1:setPasswordParam>
```

**応答**

なし
