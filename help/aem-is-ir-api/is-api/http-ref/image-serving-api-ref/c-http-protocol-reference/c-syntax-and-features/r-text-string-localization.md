---
description: テキスト文字列ローカライゼーションを使用すると、画像カタログに、同じ文字列値に対して複数のロケール固有の表現を含めることができます。
seo-description: テキスト文字列ローカライゼーションを使用すると、画像カタログに、同じ文字列値に対して複数のロケール固有の表現を含めることができます。
seo-title: テキスト文字列ローカライゼーション
solution: Experience Manager
title: テキスト文字列ローカライゼーション
topic: Scene7 Image Serving - Image Rendering API
uuid: bdff2403-e3bb-4b3f-a8d7-bb108c1fbee8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 3%

---


# テキスト文字列ローカライゼーション{#text-string-localization}

テキスト文字列ローカライゼーションを使用すると、画像カタログに、同じ文字列値に対して複数のロケール固有の表現を含めることができます。

サーバーは、`locale=`で指定されたロケールに一致する表現をクライアントに返すので、クライアント側のローカライゼーションを回避し、ISテキストリクエストで適切な`locale=`値を送信するだけでロケールを切り替えられます。

## 範囲 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

テキスト文字列ローカライゼーションは、次のカタログフィールドにローカライゼーショントークン` ^loc= *`locId`*^`を含むすべての文字列要素に適用されます。

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>カタログフィールド</b> </th> 
   <th class="entry"> <b>フィールド内の文字列要素</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet  </span> </p> </td> 
   <td> <p>変換可能な文字列を含むサブ要素(区切り文字「,」、「;」、「:」、フィールドの開始/終了」、またはその両方の組み合わせで区切られます)。 </p> <p> ローカライズ可能なフィールドの先頭の<span class="codeph"> 0xrrggbb </span>カラー値は、ローカライゼーションから除外され、変更せずに渡されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map  </span> </p> </td> 
   <td> <p><span class="codeph"> coords= </span>および<span class="codeph"> shape= </span>属性の値を除く、単一または重複で引用符で囲まれた任意の属性値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ターゲット  </span> </p> </td> 
   <td> <p><span class="codeph">ターゲットの値。*.label </span>と<span class="codeph">ターゲット。*.userdata </span>プロパティ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData  </span> </p> </td> 
   <td> <p>任意のプロパティの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 文字列構文{#section-d12320edf300409f8e17565b143acafc}

画像カタログ内のローカライゼーション対応の&#x200B;*`string`*&#x200B;要素は、1つ以上のローカライズされた文字列で構成され、各文字列の前にローカライゼーショントークンが付きます。

<table id="simpletable_CEFDAE8395E6493E902D58A7E5A25BC7"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> stringElement  </span> </span> </p> </td> 
  <td class="stentry"> <p>[ <span class="varname"> defaultString </span>]*{ <span class="varname"> localizationToken </span> <span class="varname"> localizedString </span>} </p> </td> 
 </tr> 
</table>

<table id="simpletable_0A687FA72C4C4C1AAFFCB43143C1AB3B"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizationToken  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> ^loc=  <span class="varname"> locStr  </span> ^  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> locId  </span> </span> </p> </td> 
  <td class="stentry"> <p>この<span class="varname"> localizationToken </span>に続く<span class="varname"> localizedString </span>の内部ロケールID。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> localizedString  </span> </span> </p> </td> 
  <td class="stentry"> <p>ローカライズされた文字列。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> defaultString  </span> </span> </p> </td> 
  <td class="stentry"> <p>不明なロケールに使用する文字列。 </p> </td> 
 </tr> 
</table>

*`locId`* はASCIIである必要があり、「^」を含めることはできません。

「^」は、HTTPエンコーディングの有無に関係なく、サブ文字列のどこにでも使用できます。 サーバーは、*`localizationToken`* `^loc=locId^`パターン全体を照合してサブ文字列を区切ります。

*`stringElements`* 少なくとも1つを含まないもの *`localizationToken`* は、ローカライゼーションとは見なされません。

## 変換マップ{#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` クライアントに戻す対象を決定するためにサーバーで使用 *`localizedStrings`* されるルールを定義します。これは、（`locale=`で指定された値と一致する）入力&#x200B;*`locales`*&#x200B;のリストで構成され、それぞれに内部ロケールID(*`locId`*)が1つもないかそれ以上も含まれています。 例：

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空の&#x200B;*`locId`*&#x200B;値は、*`defaultString`*&#x200B;を返す必要がある場合はそれを示します。

詳細は`attribute::LocaleStrMap`の説明を参照してください。

## 変換処理{#section-a2a8a3e5850f4f7c9d2318267afe98a2}

上の変換マップの例とリクエスト`/is/image/myCat/myItem?req=&locale=nl`を見ると、サーバーはまずロケールマップで「`nl`」を探します。 一致するエントリ`nl,N`は、各&#x200B;*`stringElement`*&#x200B;に対して`^loc=N^`でマークされた&#x200B;*`localizedString`*&#x200B;が返されることを示します。 この&#x200B;*`localizationToken`*&#x200B;が&#x200B;*`stringElement`*&#x200B;に存在しない場合は、空の値が返されます。

例えば、`catalog::UserData` for `myCat/myItem`に次の文字を含めるとします（明確にするために改行を挿入）。

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

サーバーは、このリクエスト例に応答して次を返します。

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 不明なロケール{#section-26dfeefbd60345de94bbfeaaf7741223}

上記の例では、`attribute::LocaleStrMap`のエントリに空の&#x200B;*`locale`*&#x200B;値が含まれています。 サーバーはこのエントリを使用して、変換マップで明示的に指定されていないすべての`locale=`値を処理します。

この変換マップの例では、*`defaultString`*&#x200B;がある場合は返すように指定しています。 したがって、この変換マップがリクエスト`/is/image/myCat/myItem?req=&locale=ja`に適用された場合、次のように返されます。

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**言語ファミリ**

変換マップの各&#x200B;*`locale`*&#x200B;に複数の&#x200B;*`locId`*&#x200B;値を関連付けることができます。 これにより、選択&#x200B;*`stringElements`*&#x200B;に対して、国固有または地域固有のバリエーション（米国英語と英国英語など）をサポートしながら、一般的なベースロケール（国際英語など）でほとんどのコンテンツを処理できます。

この例では、時折使用される代替スペルをサポートするために、米国固有の英語(` *`locId`* EUS`)と英国固有の英語(` *`locId`* EUK`)のサポートを追加します。 EUKまたはEUSが存在しない場合は、Eに戻ります。同様に、必要に応じてオーストリア独自のドイツのバリアント(`DAT`)が利用可能になり、ほとんどの場合、一般的なドイツ語&#x200B;*`localizedStrings`* （`D`でマーク）が返されます。

`attribute::LocaleStrMap` 次のようになります。

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

次の表に、代表的な&#x200B;*`stringElement`*&#x200B;と&#x200B;*`locale`*&#x200B;の組み合わせの出力を示します。

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
   <td> <p> <span class="codeph"> ^loc=E^English^loc=D^German  </span> </p> </td> 
   <td> <p> en,en_us, en_uk </p> <p> de, de_at, de_de </p> <p>その他 </p> </td> 
   <td> <p>英語 </p> <p>ドイツ語 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^Austrian  </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>その他 </p> </td> 
   <td> <p>英語 </p> <p>英国英語 </p> <p>ドイツ語 </p> <p>オーストリアの </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch  </span> </p> <p> この例では、<span class="varname"> locId </span> DDEが<span class="codeph"> attribute::LocaleStrMap </span>に存在しないので、この<span class="varname"> locId </span>に関連付けられたサブ文字列は返されません。 </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>その他 </p> </td> 
   <td> <p>英語 </p> <p>米国英語 </p> <p>ドイツ語 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>

