---
description: テキスト文字列のローカリゼーションを使用すると、画像カタログに同じ文字列値に対する複数のロケール固有の表現を含めることができます。
seo-description: テキスト文字列のローカリゼーションを使用すると、画像カタログに同じ文字列値に対する複数のロケール固有の表現を含めることができます。
seo-title: テキスト文字列のローカライズ
solution: Experience Manager
title: テキスト文字列のローカライズ
topic: Scene7 Image Serving - Image Rendering API
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# テキスト文字列のローカライズ{#text-string-localization}

テキスト文字列のローカリゼーションを使用すると、画像カタログに同じ文字列値に対する複数のロケール固有の表現を含めることができます。

サーバーは、で指定されたロケールに一致する表現をクライアントに返すので、クライアント側のローカリゼーションを回避し、ISテキストリクエストで適切な値を送信するだけでアプリケーションでロケ `locale=``locale=` ールを切り替えることができます。

## 範囲 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

テキスト文字列のローカリゼーションは、次のカタログフィールドにあるローカリゼーショントークン ` ^loc= *`locIdを含む`*^` 、すべての文字列要素に適用されます。

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
   <td> <p>変換可能な文字列を含むサブ要素（区切り文字「,」「;」「:」またはフィールドの開始/終了、あるいはその両方で区切られます）。 </p> <p> ローカライズ <span class="codeph"> 可能なフィー </span> ルドの最初にある0xrrggbbカラー値は、ローカリゼーションから除外され、変更なしで渡されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p>coords=属性とshape=属性の値を除く、単一引用符または二重 <span class="codeph"> 引用符で囲ま </span> れた任 <span class="codeph"> 意の属 </span> 性値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>任意のターゲットの <span class="codeph"> 値。*.labelと </span> target <span class="codeph"> 。*.userdataプロパ </span> ティ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>任意のプロパティの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 文字列構文 {#section-d12320edf300409f8e17565b143acafc}

画像カタログ内のロ *`string`* ーカリゼーションが有効な要素は、1つ以上のローカライズされた文字列で構成され、各文字列の前にローカリゼーショントークンが付きます。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement </span></span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ localizationToken <span class="varname"> localized </span> String <span class="varname"></span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> localization <span class="varname"> Token </span></span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc= <span class="varname"> locStr </span> ^ </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId </span></span> </p> </td> 
  <td class="stentry"> <p>このlocalizationTokenに続くローカライズさ <span class="varname"> れたStringの </span> 内部ロケー <span class="varname"> ルID </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> localized <span class="varname"> String </span></span> </p> </td> 
  <td class="stentry"> <p>ローカライズされた文字列。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> defaultString <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>不明なロケールで使用する文字列。 </p> </td> 
 </tr> 
</table>

*`locId`* はASCIIで、「^」を含めることはできません。

「^」は、HTTPエンコーディングの有無に関係なく、サブ文字列の任意の場所で使用できます。 サーバーはパターン全体を一致さ *`localizationToken`* せてサブ文 `^loc=locId^` 字列を区切ります。

*`stringElements`* 少なくとも1つを含まないものは、ローカリゼ *`localizationToken`* ーションの対象とは見なされません。

## 翻訳マップ {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` クライアントに戻す対象を決定するためにサーバーで使 *`localizedStrings`* 用されるルールを定義します。 入力のリスト(で指定した値 *`locales`* と一致する)で構成され、それぞれ `locale=`内部ロケールID( *`locId`*)がない。 例：

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

値が空 *`locId`* の場合は、値が返さ *`defaultString`* れる必要があることを示します。

詳しくは、の説明を参照し `attribute::LocaleStrMap` てください。

## 翻訳プロセス {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

上記の変換マップの例と要求があ `/is/image/myCat/myItem?req=&locale=nl`る場合、サーバーはまずロケールマッ `nl`プで「」を探します。 一致するエントリは、 `nl,N` それぞれに対して、でマ *`stringElement`*&#x200B;ークされ *`localizedString`* たが返されるこ `^loc=N^` とを示します。 がにな *`localizationToken`* い場合は、空 *`stringElement`*&#x200B;の値が返されます。

例えば、次の文字を含む `catalog::UserData` 場合( `myCat/myItem` 明確にするために改行を挿入)とします。

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

サーバーは、このリクエスト例に応答して次を返します。

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 不明なロケール {#section-26dfeefbd60345de94bbfeaaf7741223}

上の例では、に空 `attribute::LocaleStrMap` の値を持つエントリがあり *`locale`* ます。 サーバーは、このエントリを使用して、変換マッ `locale=` プで明示的に指定されていないすべての値を処理します。

この変換マップの例では、このような場合に、可能な場合にが返さ *`defaultString`* れるように指定しています。 したがって、この翻訳マップがリクエストに適用された場合、次のような値が返されま `/is/image/myCat/myItem?req=&locale=ja`す。

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**言語ファミリ**

複数の *`locId`* 値を変換マップ内の各値に関 *`locale`* 連付けることができます。 これにより、一般的なベースロケール（例：国際英語）でほとんどのコンテンツを処理しながら、国固有または地域固有のバリエーション（米国英語と英国英語）を *`stringElements`* 選択できるようになります。

この例では、時折使用される代替スペルをサポートするために、 ` *`US固有の英語(`* EUS`locId ` *`)とUK固有の英語(`* EUK`locId)のサポートを追加します。 EUKまたはEUSが存在しない場合は、Eに戻ります。同様に、オーストリア特有のドイツ語の異形( `DAT`)は、必要に応じて入手でき、ほとんどの場合、一般的なドイツ語(マーク *`localizedStrings`* 付き)を返す `D`一方で使用できます。

`attribute::LocaleStrMap` は次のようになります。

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

次の表に、代表的な出力と組み合わせの出力を *`stringElement`* 示し *`locale`* ます。

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de、de_de </p> <p>de_at </p> <p>その他 </p> </td> 
   <td> <p>英語 </p> <p>英国英語 </p> <p>ドイツ語 </p> <p>オーストリアの </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> この例では、 <span class="varname"> locId </span> DDEがattribute::LocaleStrMapに存在しないので、この <span class="codeph"> locIdに関連付けられ </span>たサブ文字列が返されないこ <span class="varname"></span> とに注意してください。 </p> </td> 
   <td> <p> en、en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>その他 </p> </td> 
   <td> <p>英語 </p> <p>英語（米国） </p> <p>ドイツ語 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

