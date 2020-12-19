---
description: 画像サービングでは、正規式の一致と置換ルールに基づく単純な要求前処理メカニズムがサポートされています。
seo-description: 画像サービングでは、正規式の一致と置換ルールに基づく単純な要求前処理メカニズムがサポートされています。
seo-title: ルールセットの参照
solution: Experience Manager
title: ルールセットの参照
topic: Scene7 Image Serving - Image Rendering API
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 0%

---


# ルールセットの参照{#rule-set-reference}

画像サービングでは、正規式の一致と置換ルールに基づく単純な要求前処理メカニズムがサポートされています。

事前処理ルールのコレクション（*ルールセット*）は、画像カタログまたはデフォルトのカタログに添付できます。 デフォルトのカタログ内のルールは、リクエストが特定のメイン画像カタログを識別しない場合にのみ適用されます。

リクエストの事前処理ルールでは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、リクエストがPlatform Serverのパーサーで処理される前に、リクエストのパスとクエリ部分を変更できます。 ルールは、通常、要求の不明化、ウォーターマーキングなどのカタログ属性のみで制御されるセキュリティ機能を設定および上書きするほか、サービスを特定のクライアントIPアドレスに制限する場合にも使用できます。

ルールセットは、XMLドキュメントファイルとして保存されます。 ルールセットファイルの相対パスまたは絶対パスを`attribute::RuleSetFile`で指定する必要があります。

## 一般的な構造{#section-8bcbd91ea8a946f28051bde8ad21827f}

```
 <?xml version="1.0" encoding="UTF-8"?> 
<ruleset> 
   <rule> 
      <expression> 
<varname>
  expression 
</varname></expression> 
      <substitution> 
<varname>
  substitution 
</varname></substitution> 
      <addressfilter> 
<varname>
  addressFilter 
</varname></addressfilter> 
      <header> 
<varname>
  headerValue 
</varname></header>  
   </rule> 
</ruleset>
```

有効なルールセットXMLファイルでは、実際のルールが定義されていない場合でも、`<?xml>`要素と`<ruleset>`要素は必ず必要です。

任意の数の`<rule>`要素を含む`<ruleset>`要素を1つだけ使用できます。

前処理ルールファイルの内容では、大文字と小文字が区別されます。

## ルールセットの検証{#section-d8d101a0b4d74580835e37d128d05567}

[!DNL RuleSet.xsd]のコピーがカタログフォルダーに提供され、[!DNL catalog.ini]ファイルに登録する前に、ルールセットファイルの検証に使用する必要があります。 画像サービングでは、検証に[!DNL RuleSet.xsd]の内部コピーが使用されます。

## URLの前処理{#section-2c09a2d79ada46b994857c6a7fb4c13a}

他の処理の前に、受信したHTTP要求は部分的に解析され、適用する画像カタログが決定されます。 カタログが識別されると、選択したカタログ（または特定のカタログが識別されなかった場合はデフォルトのカタログ）のルールセットが適用されます。

`<rule>`要素は、`<expression>`要素(*`expression`*)の内容と一致するように指定された順に検索されます。

`<rule>`が一致した場合は、オプションの&#x200B;*`substitution`*&#x200B;が適用され、変更された要求文字列がサーバーの要求パーサーに渡され、通常の処理が行われます。

`<ruleset>`の終わりに達したときに一致が見つからなかった場合、リクエストは変更されずにパーサーに渡されます。

## OnMatch属性{#section-ed952fa55d99422db0ee68a2b9d395d3}

デフォルトの動作は、`<rule>`要素の`OnMatch`属性を使用して変更できます。 `OnMatch` は、 `break` （デフォルト）、 `continue`またはに設定でき `error`ます。

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>要素と属性</b> </th> 
   <th class="entry"> <b>一致が発生した場合の動作</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>ルールの処理は、このルールの置き換えが適用された直後に終了します。 初期設定. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>置換が適用され、処理は次のルールで続行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>ルール処理はすぐに終了し、「リクエストが拒否されました」という応答ステータスがクライアントに返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## カタログ属性の上書き{#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` 要素では、ルールが適切に一致した場合に、対応するカタログ属性を上書きする属性を任意で定義できます。一致する複数のルールで同じ属性が設定されている場合は、最後のルールが使用されます。 ルールで制御できる属性のリストについては、` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)`要素の説明を参照してください。

## 正規式{#section-3f77bb9a265147b38c645f63ab1bad8b}

単純な文字列の一致は非常に基本的なアプリケーションで機能しますが、通常の式は必須です。 正規式は業界標準ですが、具体的な実装はインスタンスによって異なります。

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) では、画像サービングで使用される特定の正規式の実装について説明します。

## 捕捉したサブ文字列{#section-066e659406d5403599cd26ae35e80d68}

複雑なURLの変更を容易にするために、サブ文字列を丸括弧(...)で囲むことで、式内でサブ文字列を取り込むことができます。 取り込んだサブ文字列には、先頭の括弧の位置に従って、1から順に連番が付けられます。 ` $ *`n`*`を使用して、捕捉したサブ文字列を置換に挿入できます。*`n`*&#x200B;は、捕捉したサブ文字列のシーケンス番号です。

## ルールセットファイルの管理{#section-0598a608e4044bb4805fe93ceebe10a9}

カタログ属性`attribute::RuleSetFile`を使用して、各画像カタログに1つのルールセットファイルを添付できます。 ルールセットファイルはいつでも編集できますが、Image Serverは、関連付けられた画像カタログが再読み込みされた場合にのみ変更を認識します。 この再読み込みは、プラットフォームサーバーが起動または再起動されたときや、ファイルのサフィックスが[!DNL .ini]のプライマリカタログファイルが変更（「変更済み」）されたときに発生します。

## 例 {#section-aa769437d967459299b83a4bf34fe924}

**例A.画像名に「**  [!DNL _hg]」というサフィックスが付いている場合に画質設定を上げるルールを定義します。

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

ルール式では、URL文字列の末尾に「[!DNL _hg]」という大文字と小文字を区別しない一致を指定します。 サフィックスは、指定したクエリ文字列に置き換えられ、画質の設定が変更されます。 置換文字列の`?`文字は、正規式の特殊文字であるため、エスケープされます。

>[!NOTE]
>
>アンパサンド文字に必要なエンコーディング。 または、置換文字列をCDATAブロックに含めることもできます。

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**例B.** 特定のWebアプリケーションでは、クエリ文字列を使用できません。末尾のパス要素`small`、`medium`または`large`をテンプレートに変換するルールを定義し、残りのパスを画像名として使用します。 例えば、`myCat/myImage/small`は`myCat/smallTemplate?src=myCat/myImage`に変換されます。

サブ文字列を使用して、リクエストを再構成できます。

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 関連項目 {#section-9b748e7c5cff4759a70f96657bd43352}

[パッケージjava.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
