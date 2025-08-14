---
description: 画像サービングは、正規表現の一致および置換ルールに基づく単純なリクエスト前処理メカニズムをサポートしています。
solution: Experience Manager
title: ルールセットの参照
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# ルールセットの参照{#rule-set-reference}

画像サービングは、正規表現の一致および置換ルールに基づく単純なリクエスト前処理メカニズムをサポートしています。

前処理ルールのコレクション（*ルールセット*）は、画像カタログまたはデフォルトのカタログに添付できます。 デフォルトカタログのルールは、リクエストで特定のメイン画像カタログが識別されなかった場合にのみ適用されます。

リクエストの前処理ルールでは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、リク [!DNL Platform Server] ストのパーサーで処理される前に、リクエストのパスとクエリの部分を変更できます。 また、ルールを使用して、通常はカタログ属性でのみ制御される特定のセキュリティ機能（リクエストの不明化、ウォーターマーキング、特定のクライアント IP アドレスへのサービスの制限など）を設定および上書きすることもできます。

ルールセットは XML ドキュメントファイルとして保存されます。 ルールセットファイルの相対パスまたは絶対パスを `attribute::RuleSetFile` で指定する必要があります。

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

実際のルールが定義されていない場合でも、有効なルールセット XML ファイルでは `<?xml>` 要素と `<ruleset>` 要素が常に必要です。

任意の数の `<ruleset>` 要素を含む 1 つの `<rule>` 要素を使用できます。

前処理ルールファイルの内容では、大文字と小文字が区別されます。

## ルールセットの検証 {#section-d8d101a0b4d74580835e37d128d05567}

[!DNL RuleSet.xsd] のコピーはカタログフォルダーに用意されており、[!DNL catalog.ini] ファイルに登録する前にルールセットファイルを検証するために使用する必要があります。 画像サービングでは、検証に [!DNL RuleSet.xsd] の内部コピーが使用されます。

## URL の前処理 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

他の処理を行う前に、受信した HTTP リクエストを部分的に解析して、どの画像カタログを適用するかを決定します。 カタログが識別されると、選択したカタログ（特定のカタログが識別されていない場合はデフォルトのカタログ）のルールセットが適用されます。

`<rule>` 要素は、指定された順序で検索されて、`<expression>` 要素のコンテンツ（*`expression`*）と一致します。

`<rule>` が一致する場合、オプションの *`substitution`* が適用され、変更されたリクエスト文字列が通常の処理のためにサーバーのリクエストパーサーに渡されます。

`<ruleset>` の終わりに達してもマッチに成功しなかった場合、リクエストは変更されずにパーサに渡されます。

## Onmatch 属性 {#section-ed952fa55d99422db0ee68a2b9d395d3}

デフォルトの動作は `OnMatch` 要素の `<rule>` 属性で変更できます。 `OnMatch` は、`break` （デフォルト）、`continue`、`error` のいずれかに設定できます。

<table id="table_6680A81492B24CE593330DA7B0075E8F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 要素と属性 </b> </th> 
   <th class="entry"> <b> 一致が発生した場合の動作 </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="break"&gt; </span> </p> </td> 
   <td> <p>ルールの処理は、このルールの代用が適用された直後に終了します。 デフォルト。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>置換が適用され、処理は次のルールに進みます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>ルールの処理は直ちに終了し、「リクエストが拒否されました」応答ステータスがクライアントに返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## カタログ属性の上書き {#section-3f1e33a65c5346d1b4a69958c61432f3}

`rule` 要素では、オプションで、ルールが正常に一致した場合に対応するカタログ属性を上書きする属性を定義できます。 一致した複数のルールで同じ属性が設定された場合は、最後のルールが優先されます。 ルールで制御できる属性のリストについては、[rule](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md) 要素を参照してください。

## 正規表現 {#section-3f77bb9a265147b38c645f63ab1bad8b}

単純な文字列のマッチングは非常に基本的なアプリケーションで機能しますが、ほとんどの場合は正規表現が必要です。 正規表現は業界標準ですが、実装はインスタンスによって異なります。

画像サ [[!DNL package java.util.regex]](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) ビングで使用される特定の正規表現実装について説明します。

## キャプチャされた部分文字列 {#section-066e659406d5403599cd26ae35e80d68}

複雑な URL 変更を容易にするために、部分文字列を括弧（...）で囲んで式に取り込むことができます。 取り込まれた部分文字列は、先頭の括弧の位置に従って、1 から順に番号が付けられます。 取り込まれた部分文字列は、` $ *`n`*` を使用して置換に挿入できます。ここで、*`n`* は取り込まれた部分文字列のシーケンス番号です。

## 規則セットファイルの管理 {#section-0598a608e4044bb4805fe93ceebe10a9}

カタログ属性 `attribute::RuleSetFile` を使用して、各画像カタログに 1 つのルールセットファイルを添付できます。 ルールセットファイルはいつでも編集できますが、Image Server が変更を認識するのは、関連する画像カタログが再ロードされたときだけです。 この再読み込みは、platform サーバーが起動または再起動されたときや、[!DNL .ini] ファイルサフィックスを持つプライマリカタログファイルが変更または「タッチ」されてファイルの日付が変更された場合に発生します。

## 例 {#section-aa769437d967459299b83a4bf34fe924}

**例 A.** 画像名に「[!DNL _hg]」というサフィックスが付く場合に画質設定を増加させるルールを定義します。

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

ルール式は、URL 文字列の末尾に大文字と小文字を区別せずに「[!DNL _hg]」の一致を指定します。 サフィックスは、指定したクエリ文字列に置き換えられ、これにより画質設定が変更されます。 置換文字列の `?` 文字は正規表現の特殊文字なので、エスケープされることに注意してください。

>[!NOTE]
>
>アンパサンド文字に必要なエンコーディング。 または、置換文字列を CDATA ブロックで囲むこともできます。

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**例 B.** 特定の Web アプリケーションでは、クエリ文字列は許可されません。 パスの残りの部分を画像名として使用して、末尾のパス要素 `small`、`medium` または `large` をテンプレートに変換するルールを定義します。 例えば、`myCat/myImage/small` は `myCat/smallTemplate?src=myCat/myImage` に翻訳されます。

部分文字列を使用してリクエストを再構築できます。

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 関連項目 {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
