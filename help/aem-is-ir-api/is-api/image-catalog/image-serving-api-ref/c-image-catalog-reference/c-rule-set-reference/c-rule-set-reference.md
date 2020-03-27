---
description: 画像サービングでは、正規表現の一致と置換ルールに基づく単純なリクエスト前処理メカニズムがサポートされています。
seo-description: 画像サービングでは、正規表現の一致と置換ルールに基づく単純なリクエスト前処理メカニズムがサポートされています。
seo-title: ルールセットの参照
solution: Experience Manager
title: ルールセットの参照
topic: Scene7 Image Serving - Image Rendering API
uuid: 356e4939-c57d-459a-8e40-9b25e20fc0a3
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# ルールセットの参照{#rule-set-reference}

画像サービングでは、正規表現の一致と置換ルールに基づく単純なリクエスト前処理メカニズムがサポートされています。

一連の前処理ルール(ルールセット&#x200B;**)は、画像カタログまたはデフォルトのカタログに添付できます。 デフォルトのカタログ内のルールは、リクエストで特定のメイン画像カタログが識別されない場合にのみ適用されます。

リクエストの事前処理ルールでは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、リクエストがPlatform Serverのパーサーによって処理される前に、リクエストのパスやクエリ部分を変更できます。 ルールは、リクエストの不明化、ウォーターマーキング、特定のクライアントIPアドレスに対するサービスの制限など、通常はカタログ属性でのみ制御される特定のセキュリティ機能を設定および上書きする場合にも使用できます。

ルールセットはXMLドキュメントファイルとして保存されます。 ルールセットファイルの相対パスまたは絶対パスをに指定する必要がありま `attribute::RuleSetFile`す。

## 一般的な構造 {#section-8bcbd91ea8a946f28051bde8ad21827f}

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

との要 `<?xml>` 素は、 `<ruleset>` 実際のルールが定義されていない場合でも、常に有効なルールセットXMLファイルで必要です。

任意の数 `<ruleset>` の要素を含む1つの要素を `<rule>` 使用できます。

前処理ルールファイルの内容では、大文字と小文字が区別されます。

## ルールセットの検証 {#section-d8d101a0b4d74580835e37d128d05567}

のコピーはカタロ [!DNL RuleSet.xsd] グフォルダーに保存され、ルールセットファイルをファイルに登録する前に検証する際に使用し [!DNL catalog.ini] ます。 画像サービングでは、の内部コピーを検証に使用し [!DNL RuleSet.xsd] ています。

## URLの前処理 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

他の処理の前に、受信するHTTP要求が部分的に解析され、適用する画像カタログが決定されます。 カタログが識別されると、選択したカタログ（または特定のカタログが識別されなかった場合はデフォルトのカタログ）のルールセットが適用されます。

要素 `<rule>` は、要素の内容と一致するように指定された順序で検 `<expression>` 索され *`expression`*&#x200B;ます。

一致する `<rule>` 場合は、オプション *`substitution`* が適用され、変更された要求文字列がサーバーの要求パーサーに渡され、通常の処理が行われます。

の終わりに達したときに一致が成功しなかった場 `<ruleset>` 合、リクエストは変更されずにパーサーに渡されます。

## OnMatch属性 {#section-ed952fa55d99422db0ee68a2b9d395d3}

デフォルトの動作は、要素の属性を使 `OnMatch` 用して変更で `<rule>` きます。 `OnMatch` を（デフォルト）、ま `break` たはに設定で `continue`きます `error`。

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
   <td> <p>このルールの置き換えが適用された後、ルールの処理が直ちに終了します。 初期設定. </p> </td> 
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

## カタログ属性の上書き {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` 要素は、ルールが適切に一致した場合に、対応するカタログ属性を上書きする属性をオプションで定義できます。 複数の一致ルールで同じ属性が設定されている場合は、最後の属性が使用されます。 ルールで制御できる属性のリ ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)` ストについては、要素の説明を参照してください。

## 正規表現 {#section-3f77bb9a265147b38c645f63ab1bad8b}

単純な文字列の一致は非常に基本的なアプリケーションで機能しますが、ほとんどの場合は正規表現が必要です。 正規表現は業界標準ですが、具体的な実装はインスタンスによって異なります。

[ [!DNLパッケージjava.util.regex]は、画像サービ ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) ングで使用される具体的な正規表現の実装を示します。

## 取り込んだサブ文字列 {#section-066e659406d5403599cd26ae35e80d68}

複雑なURLの変更を容易にするために、サブ文字列を丸括弧(...)で囲むことで、式内でサブ文字列を取り込むことができます。 取り込まれたサブ文字列には、先頭の括弧の位置に従って1から順に番号が付けられます。 取り込んだサブ文字列は、 ` $ *`n`*`(は取り込んだサブ文字列の *`n`* シーケンス番号)を使用して置換に挿入できます。

## ルールセットファイルの管理 {#section-0598a608e4044bb4805fe93ceebe10a9}

カタログ属性を持つ各画像カタログには、1つのルールセットファイルを添付できま `attribute::RuleSetFile`す。 ルールセットファイルはいつでも編集できますが、Image Serverは、関連する画像カタログが再読み込みされた場合にのみ変更を認識します。 この再読み込みは、プラットフォームサーバーが起動または再起動されたときや、ファイルのサフィックスが付いているプライマリカタログファイルが変更または「 [!DNL .ini] 触れた」ときに、ファイルの日付を変更するたびに行われます。

## 例 {#section-aa769437d967459299b83a4bf34fe924}

**例A.** 画像名に接尾辞「 [!DNL _hg]」が付いている場合に画質設定を上げるルールを定義します。

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

ルール式では、URL文字列の末尾で大文字と小文字を区別し [!DNL _hg]ない「」の一致を指定します。 サフィックスは、指定したクエリ文字列に置き換えられ、画質の設定が変更されます。 置換文字列内の文 `?` 字は、正規表現の特殊文字であるので、エスケープされます。

>[!NOTE]
>
>アンパサンド文字に必要なエンコーディングです。 また、置換文字列をCDATAブロックで囲むこともできます。

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**例B.** 特定のWebアプリケーションでは、クエリ文字列は許可されません。 パスの残りの部分を画像名として使用し `small`て、トレ `medium`ーリング `large` パス要素、またはテンプレートに変換するルールを定義します。 例えば、はに `myCat/myImage/small` 変換されます `myCat/smallTemplate?src=myCat/myImage`。

リクエストを再構築するには、サブ文字列を使用します。

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 関連項目 {#section-9b748e7c5cff4759a70f96657bd43352}

[パッケージjava.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
