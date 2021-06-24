---
description: 画像サービングは、正規表現の一致と置換ルールに基づく、単純な要求前処理メカニズムをサポートしています。
solution: Experience Manager
title: ルールセットのリファレンス
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---

# ルールセットのリファレンス{#rule-set-reference}

画像サービングは、正規表現の一致と置換ルールに基づく、単純な要求前処理メカニズムをサポートしています。

前処理ルールのコレクション（*ルールセット*）は、画像カタログまたはデフォルトのカタログに添付できます。 デフォルトのカタログ内のルールは、リクエストが特定のメイン画像カタログを識別しない場合にのみ適用されます。

リクエストの前処理ルールでは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、リクエストのパスとクエリの部分をPlatform Serverのパーサーで処理する前に変更できます。 ルールは、通常、要求の難読化、ウォーターマーキング、特定のクライアントIPアドレスへのサービスの制限など、カタログ属性でのみ制御される特定のセキュリティ機能を設定および上書きする場合にも使用できます。

ルールセットは、XMLドキュメントファイルとして保存されます。 ルールセットファイルの相対パスまたは絶対パスを`attribute::RuleSetFile`で指定する必要があります。

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

`<?xml>`要素と`<ruleset>`要素は、実際のルールが定義されていなくても、常に有効なルールセットXMLファイルに必要です。

任意の数の`<rule>`要素を含む`<ruleset>`要素を1つ使用できます。

前処理ルールファイルの内容では、大文字と小文字が区別されます。

## ルールセットの検証 {#section-d8d101a0b4d74580835e37d128d05567}

[!DNL RuleSet.xsd]のコピーがカタログフォルダーに提供され、[!DNL catalog.ini]ファイルに登録する前にrulesetファイルを検証するために使用する必要があります。 画像サービングでは、検証に[!DNL RuleSet.xsd]の内部コピーが使用されます。

## URLの前処理 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

他の処理の前に、受信HTTPリクエストが部分的に解析されて、適用する画像カタログが決定されます。 カタログが識別されると、選択したカタログ（特定のカタログが識別されなかった場合はデフォルトのカタログ）のルールセットが適用されます。

`<rule>`要素は、`<expression>`要素(*`expression`*)の内容と一致するように指定された順序で検索されます。

`<rule>`が一致する場合は、オプションの&#x200B;*`substitution`*&#x200B;が適用され、変更されたリクエスト文字列が通常の処理のためにサーバーのリクエストパーサーに渡されます。

`<ruleset>`の終わりに達しても一致が見つからない場合、リクエストは変更されずにパーサーに渡されます。

## OnMatch属性 {#section-ed952fa55d99422db0ee68a2b9d395d3}

デフォルトの動作は、`<rule>`要素の`OnMatch`属性で変更できます。 `OnMatch` は（デフォルト）、 `break` または `continue`に設定できま `error`す。

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
   <td> <p>ルールの処理は、このルールの置換が適用された直後に終了します。 初期設定. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>置換が適用され、次のルールで処理が続行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>ルールの処理は直ちに終了し、「リクエスト拒否」応答ステータスがクライアントに返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## カタログ属性の上書き {#section-3f1e33a65c5346d1b4a69958c61432f3}

`<rule>` 要素では、オプションで、ルールが正しく一致した場合に対応するカタログ属性を上書きする属性を定義できます。一致する複数のルールが同じ属性を設定する場合は、最後のルールが優先されます。 ルールで制御できる属性のリストについては、 ` [<rule>](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md#reference-af76c0e2b8be48dabb52b71fe7e51ee9)`要素の説明を参照してください。

## 正規表現 {#section-3f77bb9a265147b38c645f63ab1bad8b}

単純な文字列のマッチングは非常に基本的なアプリケーションで機能しますが、ほとんどの場合、正規表現が必要です。 正規表現は業界標準ですが、実装はインスタンスによって異なります。

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) は、画像サービングで使用される特定の正規表現の実装について説明します。

## 取り込まれたサブ文字列 {#section-066e659406d5403599cd26ae35e80d68}

複雑なURLの変更を容易にするために、サブ文字列を括弧(...)で囲むことで、式にサブ文字列を取り込むことができます。 取り込まれたサブ文字列には、先頭の括弧の位置に従って1から順に番号が付けられます。 ` $ *`n`*`を使用して、取り込んだサブ文字列を置換に挿入できます。*`n`*&#x200B;は、取り込んだサブ文字列のシーケンス番号です。

## ルールセットファイルの管理 {#section-0598a608e4044bb4805fe93ceebe10a9}

カタログ属性`attribute::RuleSetFile`を使用して、各画像カタログに1つのルールセットファイルを添付できます。 ルールセットファイルはいつでも編集できますが、Image Serverは、関連する画像カタログが再読み込みされた場合にのみ変更を認識します。 この再読み込みは、プラットフォームサーバーが起動または再起動されたときや、[!DNL .ini]ファイルサフィックスを持つプライマリカタログファイルが、ファイルの日付を変更するために変更または「touched」されるたびに発生します。

## 例 {#section-aa769437d967459299b83a4bf34fe924}

**例A.** 画像名に「 」というサフィックスが付く場合に画質設定を増やすルールを定義 [!DNL _hg]します。

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

ルール式は、URL文字列の末尾で「 [!DNL _hg] 」という大文字と小文字を区別しない一致を指定します。 サフィックスは、画質設定を変更する指定されたクエリ文字列に置き換えられます。 置換文字列内の`?`文字は正規表現の特殊文字なので、エスケープされます。

>[!NOTE]
>
>アンパサンド文字に必要なエンコーディング。 または、置換文字列をCDATAブロックに含めることもできます。

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**例B.** 特定のWebアプリケーションではクエリー文字列を許可しません。パスの残りの部分を画像名として使用して、末尾のパス要素`small`、`medium`または`large`をテンプレートに変換するルールを定義します。 例えば、`myCat/myImage/small`は`myCat/smallTemplate?src=myCat/myImage`に変換されます。

サブ文字列を使用して、リクエストを再構築できます。

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 関連項目 {#section-9b748e7c5cff4759a70f96657bd43352}

[パッケージjava.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
