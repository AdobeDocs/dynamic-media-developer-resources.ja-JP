---
title: テキスト文字列のローカライズ
description: テキスト文字列のローカリゼーションを使用すると、画像カタログに、同じ文字列値に対してロケール固有の複数の表現を含めることができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f105c7f2-b544-4c08-bb91-4916e485572d
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '644'
ht-degree: 1%

---

# テキスト文字列のローカライズ{#text-string-localization}

テキスト文字列のローカリゼーションを使用すると、画像カタログに、同じ文字列値に対してロケール固有の複数の表現を含めることができます。

サーバーは、`locale=` で指定されたロケールに一致する表現をクライアントに返します。これにより、クライアント側でのローカリゼーションが回避され、IS テキスト要求で適切な `locale=` 値を送信するだけでロケールを切り替えることができます。

## 範囲 {#section-a03f48e3bc0e4ab281909a2bd441a3c2}

テキスト文字列のローカリゼーションは、次のカタログフィールドにローカリゼーショントークン ` ^loc= *`locId`*^` を含むすべての文字列要素に適用されます。

<table id="table_83344EFCB5B5418184E0A0B43D0B23F7"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> カタログフィールド </b> </th> 
   <th class="entry"> <b> フィールドの文字列要素 </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::ImageSet </span> </p> </td> 
   <td> <p>翻訳可能な文字列を含むすべてのサブ要素（区切り文字「,」「;」「:」やフィールドの開始/終了の任意の組み合わせで区切られる）。 </p> <p> ローカライズ可能なフィールドの先頭にある <span class="codeph"> 0xrggbb </span> color 値は、ローカライズから除外され、変更なしで渡されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Map </span> </p> </td> 
   <td> <p><span class="codeph"> coords= </span> および <span class="codeph"> shape= </span> 属性の値を除く、一重引用符または二重引用符で囲まれた属性値。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::Targets </span> </p> </td> 
   <td> <p>任意の <span class="codeph"> ターゲットの値。*.label </span> と <span class="codeph"> target。*.userdata </span> プロパティ。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> catalog::UserData </span> </p> </td> 
   <td> <p>プロパティの値。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 文字列構文 {#section-d12320edf300409f8e17565b143acafc}

画像カタログ内のローカライゼーションが有効な *`string`* 要素は、1 つ以上のローカライズされた文字列で構成され、各文字列の前にはローカライゼーショントークンが付きます。

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
  <td class="stentry"> <p>この <span class="varname"> localizationToken </span> に続く <span class="varname"> localizedString の内部ロケール ID</span> す。 </p> </td> 
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

*`locId`* は ASCII である必要があり、「^」を含めることはできません。

「^」は、HTTP エンコーディングの有無に関わらず、部分文字列のどこにでも存在する可能性があります。 サーバーは、*`localizationToken`* `^loc=locId^` パターン全体を照合して、サブ文字列を区切ります。

*`stringElements`* には 1 つ以上の *`localizationToken`* が含まれていないので、ローカライズの対象にはなりません。

## 翻訳マップ {#section-f7ce3df91b724adf95cee44eac4915d4}

`attribute::LocaleStrMap` は、クライアントに返す *`localizedStrings`* を決定するためにサーバーが使用するルールを定義します。 これは入力 *`locales`* のリスト（`locale=` で指定された値に一致）で構成され、それぞれに内部ロケール ID （*`locId`*）が 0 個以上あります。 以下に例を挙げます。

`attribute::LocaleStrMap= en,E|nl,N|de,D|,`

空の *`locId`* 値は、*`defaultString`* が返される必要があることを示します（使用可能な場合）。

詳しくは、`attribute::LocaleStrMap` の説明を参照してください。

## 翻訳プロセス {#section-a2a8a3e5850f4f7c9d2318267afe98a2}

上記の翻訳マップの例とリクエスト `/is/image/myCat/myItem?req=&locale=nl` を指定すると、サーバーはまず、ロケールマップで「`nl`」を探します。 一致するエントリ `nl,N` は、*`stringElement`* ごとに、`^loc=N^` でマークされた *`localizedString`* を返す必要があることを示しています。 この *`localizationToken`* が *`stringElement`* に存在しない場合は、空の値が返されます。

例えば、`myCat/myItem` の `catalog::UserData` に次の改行が含まれているとします（わかりやすくするために挿入されます）。

`val1=111?? str1=Default1^loc=N^Dutch1^loc=D^German1?? val2=value2?? str2=^loc=E^English2^loc=N^Dutch2^loc=D^German2?? str3=Default3^loc=N^Dutch3^loc=D^German3`

サーバーは、サンプルのリクエストに応答して次を返します。

`val1=111 str1=Dutch1 val2=value2 str2=Dutch2 str3=Dutch3`

## 不明なロケール {#section-26dfeefbd60345de94bbfeaaf7741223}

上記の例では、`attribute::LocaleStrMap` には、空の *`locale`* 値を持つエントリがあります。 サーバーはこのエントリを使用して、翻訳マップで明示的に指定されていないすべての `locale=` 値を処理します。

翻訳マップの例では、このような場合に *`defaultString`* が返されるように指定しています（使用可能な場合）。 したがって、この翻訳マップがリクエスト `/is/image/myCat/myItem?req=&locale=ja` ージに適用される場合は、次のように返されます。

`val1=111 str1=Default1 val2=value2 str2= str3=Default3`

## 例 {#section-ae6ff7fb90754b839f04ed08aadffa3f}

**言語ファミリ**

複数の *`locId`* 値を翻訳マップの各 *`locale`* に関連付けることができます。 その理由は、選択した *`stringElements`* ーザーに対して国固有または地域固有のバリエーション（例：米国英語と英国英語）をサポートし、共通の基本ロケール（例：国際英語）を使用してほとんどのコンテンツを処理できるためです。

例えば、米国固有の英語（`*`locId`* EUS`）と英国固有の英語（`*`locId`* EUK`）のサポートが追加され、時折の代替スペルがサポートされます。 EUK または EUS が存在しない場合は、E にフォールバックします。同様に、オーストリア固有のドイツ語版（`DAT`）を必要に応じて使用できるようにし、その際に一般的なドイツ語 *`localizedStrings`* （`D` でマーク）を常に返すことができます。

`attribute::LocaleStrMap` は次のようになります。

`en,E|en_us,EUS,E|en_uk,EUK,E|de,D|de_at,DAT,D|de_de,D`

次の表に、代表的な *`stringElement`* と *`locale`* の組み合わせの出力を示します。

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
   <td> <p> en, en_us, en_uk </p> <p> de, de_at, de_de </p> <p>その他すべて </p> </td> 
   <td> <p>英語 </p> <p>ドイツ語 </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^loc=E^English^loc=UKE^UK-English^loc=D^German^loc=DAT^オーストリア </span> </p> </td> 
   <td> <p> en, en_us </p> <p> en_uk </p> <p> de, de_de </p> <p>de_at </p> <p>その他すべて </p> </td> 
   <td> <p>英語 </p> <p>英国 – 英語 </p> <p>ドイツ語 </p> <p>オーストリア </p> <p>- </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ^ loc=en^English^loc=USE^US-English^loc=D^German^loc=DDE^Deutsch </span> </p> <p> この例では、<span class="varname"> locId</span>DDE は attribute::LocaleStrMap </span> に存在 <span class="codeph"> ないので、この <span class="varname"> locId </span> に関連付けられた部分文字列は返されません。 </p> </td> 
   <td> <p> en, en_uk </p> <p> en_us </p> <p> de, de_at, de_de </p> <p>その他すべて </p> </td> 
   <td> <p>英語 </p> <p>米国 – 英語 </p> <p>ドイツ語 </p> <p>- </p> </td> 
  </tr> 
 </tbody> 
</table>
