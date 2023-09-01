---
title: テキスト文字列のローカライゼーション
description: テキスト文字列のローカリゼーションを使用すると、画像カタログに同じ文字列値に対して、複数のロケール固有の表現を含めることができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '669'
ht-degree: 3%

---

# テキスト文字列のローカライゼーション{#text-string-localization}

テキスト文字列のローカリゼーションを使用すると、画像カタログに同じ文字列値に対して、複数のロケール固有の表現を含めることができます。

サーバーは、で指定されたロケールに一致する表現をクライアントに返します。 `locale=`クライアント側のローカライゼーションを回避し、適切な `locale=` の値に、IS テキストリクエストを含めます。

## 範囲 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

テキスト文字列のローカライゼーションは、ローカライゼーショントークンを含むすべての文字列要素に適用されます ` ^loc= *`locId`*^` 次のカタログフィールド内：

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>カタログフィールド</b> </th> 
   <th class="entry"> <b>フィールド内の文字列要素</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>翻訳可能な文字列を含むサブ要素（区切り文字「,」、「;」、「:」、フィールドの開始/終了の組み合わせで区切られます）。 </p> <p> A <span class="codeph"> 0xrrggbb </span> ローカライズ可能フィールドの先頭の色の値は、ローカライゼーションから除外され、変更されずに渡されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>引用符で囲まれた単一または二重引用符で囲まれた任意の属性値 ( <span class="codeph"> coords= </span> および <span class="codeph"> shape= </span> 属性。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>任意の <span class="codeph"> ターゲット。*.label </span> および <span class="codeph"> ターゲット。*.userdata </span> プロパティ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>任意のプロパティの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 文字列の構文 {#section-d12320edf300409f8e17565b143acafc}

ローカリゼーション対応 *`string`* 画像カタログ内の要素は、1 つ以上のローカライズされた文字列で構成され、それぞれの前にローカライゼーショントークンが付きます。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span> </span> </p> </td> 
  <td class="stentry"> <p>の内部ロケール ID <span class="varname"> localizedString </span> この後 <span class="varname"> localizationToken </span>. </p> </td> 
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

The *`locId`* は ASCII にする必要があり、「^」を含めることはできません。

「^」は、HTTP エンコーディングの有無に関わらず、サブ文字列の任意の場所に配置できます。 サーバーは、 *`localizationToken`* `^loc=locId^` パターンを使用して部分文字列を区切ります。

The *`stringElements`*（少なくとも 1 つを含まない） *`localizationToken`*&#x200B;をローカライゼーションの対象としない場合は考慮されません。

## 翻訳マップ {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` は、どのルールを決定するためにサーバーで使用されるルールを定義します *`localizedStrings`* をクライアントに戻します。 入力のリストで構成されます。 *`locales`* ( `locale=`) の代わりに、内部ロケール ID( *`locId`*) をクリックします。 以下に例を挙げます。

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空 *`locId`* 値は、 *`defaultString`* を返す必要があります（存在する場合）。

詳しくは、 `attribute::LocaleStrMap` 」を参照してください。

## 翻訳プロセス {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

上記の翻訳マップの例と要求 `/is/image/myCat/myItem?req=&locale=nl`を検索する場合、サーバーは最初に「 `nl`」がロケールマップに表示されます。 一致したエントリ `nl,N` は、 *`stringElement`*、 *`localizedString`* ～で特徴付けられる `^loc=N^` を返す必要があります。 次の場合、 *`localizationToken`* が *`stringElement`*&#x200B;の場合、空の値が返されます。

例えば、 `catalog::UserData` 対象： `myCat/myItem` には次の文字が含まれます（分かりやすくするために挿入された改行）。

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

サーバーは、このリクエスト例に応じて次の応答を返します。

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 不明なロケール {#section-26dfeefbd60345de94bbfeaaf7741223}

上記の例では、 `attribute::LocaleStrMap` には、空の *`locale`* の値です。 サーバーは、このエントリを使用してすべての `locale=` 翻訳マップで明示的に指定されていない値。

翻訳マップの例では、この場合、 *`defaultString`* を返す必要があります（存在する場合）。 したがって、この翻訳マップがリクエストに適用されると、次の値が返されます。 `/is/image/myCat/myItem?req=&locale=ja`:

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**言語ファミリー**

複数 *`locId`* 値は、 *`locale`* 翻訳マップ内で使用します。 これは、国固有または地域固有のバリエーション（例えば、米国英語と英国英語）を選択できるからです。 *`stringElements`* では、一般的な基本ロケール（例えば、国際英語）を使用したほとんどのコンテンツを処理します。

この例では、米国固有の英語 ( `*`locId`* EUS`) および UK 固有の英語 ( `*`locId`* EUK`) を使用して、時折使用される代替スペルをサポートします。 EUK または EUS が存在しない場合は、E.にフォールバックします。同様に、オーストリア特有のドイツ系 ( `DAT`) は、必要に応じて利用できるようにし、一般的なドイツ語を返す *`localizedStrings`* ( `D`) ほとんどの場合に使用されます。

The `attribute::LocaleStrMap` 次のようになります。

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

次の表に、代表者の出力を示します。 *`stringElement`* および *`locale`* 組み合わせ：

<table id="table_A6B67587C5F44B5E9CD0E7ED29A81198"> 
 <thead> 
  <tr> 
   <th class="entry"> <i>stringElement</i> </th> 
   <th class="entry"> <i>locale</i> </th> 
   <th class="entry"> <p>出力文字列 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>その他 </p> </td> 
   <td> <p>英語 </p> <p>ドイツ語 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UK^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de_de </p> <p>de_at </p> <p>その他 </p> </td> 
   <td> <p>英語 </p> <p>UK-English </p> <p>ドイツ語 </p> <p>オーストリア語 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> この例では、 <span class="varname"> locId </span> DDE が次に存在しません： <span class="codeph"> attribute::LocaleStrMap </span>の部分文字列で、この <span class="varname"> locId </span> が返されない。 </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>その他 </p> </td> 
   <td> <p>英語 </p> <p>US-English </p> <p>ドイツ語 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
