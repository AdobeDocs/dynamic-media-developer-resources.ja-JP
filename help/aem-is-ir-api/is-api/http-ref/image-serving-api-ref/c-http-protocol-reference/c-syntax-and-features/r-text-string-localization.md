---
title: テキスト文字列のローカライズ
description: テキスト文字列のローカライゼーションを使用すると、画像カタログに、同じ文字列値に対する複数のロケール固有の表現を含めることができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
TQID: 'https://experienceleague.adobe.com/iT-q5yLQijvkYDB0xOq3E6r1k3DIbU9BWu3Jkqs8wUI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 672
ht-degree: 1%

---

# テキスト文字列のローカライズ{#text-string-localization}

テキスト文字列のローカライゼーションを使用すると、画像カタログに、同じ文字列値に対する複数のロケール固有の表現を含めることができます。

サーバーは、`locale=`で指定されたロケールに一致する表現をクライアントに返します。クライアント側のローカライゼーションは避け、アプリケーションはIS テキストリクエストで適切な`locale=`値を送信するだけでロケールを切り替えることができます。

## 範囲 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

テキスト文字列のローカライズは、次のカタログフィールドにローカライゼーショントークン ` ^loc= *`locId`*^`を含むすべての文字列要素に適用されます。

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> カタログフィールド </b> </th> 
   <th class="entry"> フィールド </b>の<b>文字列要素 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：:ImageSet </span> </p> </td> 
   <td> <p>翻訳可能な文字列を含むサブエレメント（区切り記号「,」「;」「:」および/またはフィールドの開始/終了の任意の組み合わせで区切られます）。 </p> <p> ローカライズ可能なフィールドの先頭にある<span class="codeph"> 0xrrggbb </span>のカラー値は、ローカライズから除外され、変更なしで渡されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：：マップ </span> </p> </td> 
   <td> <p><span class="codeph"> coords= </span>および<span class="codeph"> shape= </span>属性の値を除く、任意の一重引用符または二重引用符で囲まれた属性値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：：ターゲット </span> </p> </td> 
   <td> <p>任意の<span class="codeph"> target.*.label </span>および<span class="codeph"> target.*.userdata </span> プロパティの値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> カタログ：:UserData </span> </p> </td> 
   <td> <p>任意のプロパティの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 文字列構文 {#section-d12320edf300409f8e17565b143acafc}

画像カタログ内のローカライズ可能な&#x200B;*`string`*&#x200B;要素は、1つ以上のローカライズされた文字列で構成され、それぞれにローカライズトークンが先行します。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[<span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>この<span class="varname"> localizationToken </span>に続く<span class="varname"> localizedString </span>の内部ロケール ID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString </span> </span> </p> </td> 
  <td class="stentry"> <p>ローカライズされた文字列。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString </span> </span> </p> </td> 
  <td class="stentry"> <p>不明なロケールに使用する文字列。 </p> </td> 
 </tr> 
</table>

*`locId`*&#x200B;はASCIIである必要があり、&#39;^&#39;を含めることはできません。

「^」は、HTTP エンコーディングの有無にかかわらず、サブストリング内のどこでも発生する可能性があります。 サーバーは、*`localizationToken`* `^loc=locId^` パターン全体を別々のサブストリングに一致させます。

少なくとも1つの&#x200B;*`localizationToken`*&#x200B;を含まない&#x200B;*`stringElements`*&#x200B;は、ローカライズには考慮されません。

## 翻訳マップ {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap`は、クライアントに返す&#x200B;*`localizedStrings`*&#x200B;を決定するためにサーバーが使用するルールを定義します。 これは、入力&#x200B;*`locales`* （指定された値と`locale=`に一致）のリストで構成され、それぞれに内部ロケール ID （*`locId`*）が含まれていません。 以下に例を挙げます。

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空の&#x200B;*`locId`*&#x200B;値は、*`defaultString`*&#x200B;が返されることを示します（使用可能な場合）。

詳しくは、`attribute::LocaleStrMap`の説明を参照してください。

## 翻訳プロセス {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

上記の翻訳マップの例とリクエスト `/is/image/myCat/myItem?req=&locale=nl`を考えると、サーバーは最初にロケールマップで「`nl`」を探します。 一致するエントリ `nl,N`は、各&#x200B;*`stringElement`*&#x200B;について、`^loc=N^`でマークされた&#x200B;*`localizedString`*&#x200B;を返すことを示します。 この&#x200B;*`localizationToken`*&#x200B;が&#x200B;*`stringElement`*&#x200B;に存在しない場合、空の値が返されます。

例えば、`myCat/myItem`の`catalog::UserData`に次の内容が含まれているとします（明確化のために改行が挿入されています）。

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

サーバーは、リクエストの例に応じて次の値を返します。

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 不明なロケール {#section-26dfeefbd60345de94bbfeaaf7741223}

上記の例では、`attribute::LocaleStrMap`には空の&#x200B;*`locale`*&#x200B;値を持つエントリがあります。 サーバーはこのエントリを使用して、翻訳マップで明示的に指定されていないすべての`locale=`値を処理します。

翻訳マップの例では、このような場合に&#x200B;*`defaultString`*&#x200B;が返されるように指定します（使用可能な場合）。 したがって、この翻訳マップがリクエスト `/is/image/myCat/myItem?req=&locale=ja`に適用された場合、次が返されます。

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**言語ファミリー**

翻訳マップの各&#x200B;*`locale`*&#x200B;に複数の&#x200B;*`locId`*&#x200B;値を関連付けることができます。 その理由は、共通のベースロケール （国際英語など）を持つほとんどのコンテンツを処理しながら、一部の&#x200B;*`stringElements`*&#x200B;の国固有または地域固有のバリエーション （例：米国英語と英国英語）をサポートできるためです。

例えば、米国固有の英語（`*`locId`* EUS`）および英国固有の英語（`*`locId`* EUK`）に対して、時折代替スペルをサポートするサポートが追加されています。 EUKまたはEUSが存在しない場合は、Eにフォールバックします。同様に、オーストリア固有のドイツ語のバリエーション（`DAT`）を必要に応じて利用できるようにしながら、一般的なドイツ語&#x200B;*`localizedStrings`* （`D`でマーク）をほとんどの場合に返すことができます。

`attribute::LocaleStrMap`は次のようになります。

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

次の表は、代表的な&#x200B;*`stringElement`*&#x200B;と&#x200B;*`locale`*&#x200B;の組み合わせの出力を示しています。

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i> ロケール </i> </th> 
   <th class="entry"> <p>出力文字列 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>その他 </p> </td> 
   <td> <p>英語 </p> <p>ドイツ語 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>その他 </p> </td> 
   <td> <p>英語 </p> <p>UK-English </p> <p>ドイツ語 </p> <p>オーストリア語 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> この例では、<span class="varname"> locId </span> DDEが<span class="codeph">属性：:LocaleStrMap </span>に存在しないため、この<span class="varname"> locId </span>に関連付けられた部分文字列は返されません。 </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>その他 </p> </td> 
   <td> <p>英語 </p> <p>US-English </p> <p>ドイツ語 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
