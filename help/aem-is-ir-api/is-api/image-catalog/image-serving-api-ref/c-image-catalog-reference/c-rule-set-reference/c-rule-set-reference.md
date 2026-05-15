---
description: 画像サービングは、正規表現の一致と置換ルールに基づくシンプルなリクエスト前処理メカニズムをサポートしています。
solution: Experience Manager
title: ルールセット参照
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
TQID: 'https://experienceleague.adobe.com/ZRyGq2UXh41F4IpGudN48CV0LxzrDjZKk2yaOQnUP3o'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 808
ht-degree: 0%

---

# ルールセット参照{#rule-set-reference}

画像サービングは、正規表現の一致と置換ルールに基づくシンプルなリクエスト前処理メカニズムをサポートしています。

前処理ルールのコレクション（*ルールセット*）は、画像カタログまたはデフォルトカタログに添付できます。 デフォルトカタログのルールは、リクエストが特定のメイン画像カタログを識別しない場合にのみ適用されます。

リクエスト前処理ルールは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、[!DNL Platform Server]のパーサーによって処理される前に、リクエストのパスとクエリ部分を変更できます。 また、ルールを使用して、リクエストの難読化、ウォーターマーク、特定のクライアント IP アドレスへのサービス制限など、通常はカタログ属性でのみ制御される特定のセキュリティ機能を設定および上書きすることもできます。

ルールセットは、XML ドキュメントファイルとして保存されます。 ルール セット ファイルの相対パスまたは絶対パスを`attribute::RuleSetFile`で指定する必要があります。

## 一般構造 {#section-8bcbd91ea8a946f28051bde8ad21827f}

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

実際のルールが定義されていない場合でも、有効なルールセット XML ファイルでは`<?xml>`要素と`<ruleset>`要素が常に必要です。

任意の数の`<rule>`要素を含む1つの`<ruleset>`要素を使用できます。

前処理ルールファイルの内容では、大文字と小文字が区別されます。

## ルールセットの検証 {#section-d8d101a0b4d74580835e37d128d05567}

[!DNL RuleSet.xsd]のコピーはカタログ フォルダーに提供されます。ルールセット ファイルを検証してから[!DNL catalog.ini] ファイルに登録する必要があります。 画像サービングでは、検証に[!DNL RuleSet.xsd]の内部コピーが使用されていることに注意してください。

## URLの事前処理 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

他の処理の前に、受信HTTP リクエストが部分的に解析され、どの画像カタログを適用するかを決定します。 カタログが識別されると、選択したカタログのルールセット（または特定のカタログが識別されていない場合はデフォルトのカタログ）が適用されます。

`<rule>`要素は、`<expression>`要素（*`expression`*）の内容と一致するように指定された順序で検索されます。

`<rule>`が一致する場合、オプションの&#x200B;*`substitution`*&#x200B;が適用され、変更されたリクエスト文字列が通常の処理のためにサーバーのリクエストパーサーに渡されます。

`<ruleset>`の末尾に到達したときに一致が成功しなかった場合、リクエストは変更なしでパーサーに渡されます。

## OnMatch属性 {#section-ed952fa55d99422db0ee68a2b9d395d3}

デフォルトの動作は、`<rule>`要素の`OnMatch`属性で変更できます。 `OnMatch`は`break` （デフォルト）、`continue`、または`error`に設定できます。

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
   <td> <p>ルール処理は、このルールの代用が適用された直後に終了します。 デフォルト： </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="continue"&gt; </span> </p> </td> 
   <td> <p>置換が適用され、処理は次のルールで続行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>ルール処理は直ちに終了し、「リクエスト拒否」応答ステータスがクライアントに返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## カタログ属性の上書き {#section-3f1e33a65c5346d1b4a69958c61432f3}

`rule`要素は、ルールが正常に一致したときに、対応するカタログ属性を上書きする属性をオプションで定義できます。 複数の一致したルールが同じ属性を設定する場合は、最後のルールが優先されます。 ルールで制御できる属性のリストについては、[&#x200B; ルール &#x200B;](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md)要素を参照してください。

## 正規表現 {#section-3f77bb9a265147b38c645f63ab1bad8b}

単純な文字列マッチングは、非常に基本的なアプリケーションで機能しますが、ほとんどの場合、正規表現が必要です。 正規表現は業界標準ですが、具体的な実装はインスタンスによって異なります。

[[!DNL package java.util.regex]](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)は、画像サービングで使用される特定の正規表現の実装について説明します。

## キャプチャされたサブストリング {#section-066e659406d5403599cd26ae35e80d68}

複雑なURLの変更を容易にするために、サブストリングを括弧（。..）で囲むことで、エクスプレッションにサブストリングを取り込むことができます。 キャプチャされたサブストリングには、先頭の括弧の位置に従って、1から始まる番号が付けられます。 キャプチャされたサブストリングは、` $ *`n`*`を使用して置換に挿入できます。ここで、*`n`*&#x200B;はキャプチャされたサブストリングのシーケンス番号です。

## ルールセットファイルの管理 {#section-0598a608e4044bb4805fe93ceebe10a9}

カタログ属性`attribute::RuleSetFile`を持つ各画像カタログには、1つのルール セット ファイルを添付できます。 ルールセットファイルはいつでも編集できますが、関連する画像カタログが再ロードされたときにのみ、画像サーバーは変更を認識します。 この再読み込みは、プラットフォームサーバーが起動または再起動されたときに行われ、ファイルのサフィックスが[!DNL .ini]のプライマリカタログファイルが変更または「タッチ」されてファイルの日付が変更されるたびに行われます。

## 例 {#section-aa769437d967459299b83a4bf34fe924}

**例A.**&#x200B;画像名に接尾辞「[!DNL _hg]」が付いている場合に、画質設定を増やすルールを定義します。

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

ルール式では、URL文字列の末尾に「[!DNL _hg]」の大文字と小文字を区別しない一致が指定されます。 接尾辞は、指定したクエリ文字列に置き換えられ、画質設定が変更されます。 置換文字列内の`?`文字は、正規表現の特殊文字であるため、エスケープされることに注意してください。

>[!NOTE]
>
>アンパサンド文字に必要なエンコーディング。 代わりに、置換文字列をCDATA ブロックで囲むこともできます。

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**例B.** 特定のweb アプリケーションでは、クエリ文字列を許可していません。 末尾のパス要素`small`、`medium`または`large`をテンプレートに変換するルールを定義します。このルールでは、パスの残りの部分を画像名として使用します。 例えば、`myCat/myImage/small`は`myCat/smallTemplate?src=myCat/myImage`に変換されます。

サブストリングを使用して、リクエストを再構築できます。

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 関連項目 {#section-9b748e7c5cff4759a70f96657bd43352}

[パッケージ java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
