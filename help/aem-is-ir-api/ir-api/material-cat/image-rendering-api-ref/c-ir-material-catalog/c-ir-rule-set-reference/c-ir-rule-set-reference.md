---
description: 画像レンダリングは、正規表現の一致と置換ルールに基づく単純なリクエストの前処理メカニズムをサポートしています。
seo-description: 画像レンダリングは、正規表現の一致と置換ルールに基づく単純なリクエストの前処理メカニズムをサポートしています。
seo-title: ルールセットの参照
solution: Experience Manager
title: ルールセットの参照
topic: Scene7 Image Serving - Image Rendering API
uuid: aeec7597-4d23-4cf8-8bdc-3a133152eadb
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba

---


# ルールセットの参照{#rule-set-reference}

画像レンダリングは、正規表現の一致と置換ルールに基づく単純なリクエストの前処理メカニズムをサポートしています。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

事前処理ルール(ルールセット&#x200B;**)のコレクションは、マテリアルカタログまたはデフォルトのカタログに添付できます。 リクエストが特定の材料カタログをアタッチしない場合にのみ、デフォルトのカタログのルールが適用されます。

リクエストの事前処理ルールでは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、リクエストがサーバーのリクエストパーサーによって処理される前に、リクエストのパスやクエリ部分を変更できます。 ルールは、一部のカタログ属性の設定と上書き、およびサービスを特定のクライアントIPアドレスに制限する場合にも使用できます。

ルールセットはXMLドキュメントファイルとして保存されます。 ルールセットファイルの相対パスまたは絶対パスをに指定する必要がありま `attribute::RuleSetFile`す。

## 一般的な構造 {#section-74faaee27fc543a2ab4a306f3a03674e}

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE ruleset SYSTEM" RuleSet.dtd">
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
   </rule>
</ruleset>
```

、および `<?xml>`の要 `<!DOCTYPE>` 素は、 `<ruleset>` 実際のルールが定義されていない場合でも、常に有効なルールセットXMLファイルで必要です。

任意の数 `<ruleset>` の要素を含む1つの要素を `<rule>` 使用できます。

前処理ルールファイルの内容では、大文字と小文字が区別されます。

## URLの前処理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

他の処理の前に、受信したHTTP要求が部分的に解析され、適用する材料カタログが決定されます。 カタログが識別されると、選択したカタログ（または特定のカタログが識別されなかった場合はデフォルトのカタログ）のルールセットが適用されます。

要素 `<rule>` は、要素の内容と一致するように指定された順序で検 `<expression>` 索され *`expression`*&#x200B;ます。

一致する `<rule>` 場合は、オプション *`substitution`* が適用され、変更された要求文字列がサーバーの要求パーサーに渡され、通常の処理が行われます。

の終わりに達したときに一致が成功しなかった場 `<ruleset>` 合、リクエストは変更されずにパーサーに渡されます。

## OnMatch属性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

デフォルトの動作は、要素の属性を使 `OnMatch` 用して変更で `<rule>` きます。 `OnMatch` を（デフォルト）に設 `break` 定するか、または `continue`に設定する `error.`

<table id="table_4CABF55B33854A128D5F326B31C6C397"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>要素と属性 </p> </th> 
   <th colname="col2" class="entry"> <p>一致が発生した場合の動作 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="break"&gt;</span> </p> </td> 
   <td colname="col2"> <p>このルールの置き換えが適用された後、ルールの処理が直ちに終了します。 初期設定. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>置換が適用され、処理は次のルールで続行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>ルール処理はすぐに終了し、「リクエストが拒否されました」という応答ステータスがクライアントに返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## カタログ属性の上書き {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 要素では、ルールが適切に一致し、設定された場合に、対応するカタログ属性を上書きする属性を任意で定 `OnMatch="break"` 義できます。 を設定した場合、属性は適用 `OnMatch="continue"` されません。 ルールで制御できる属 `<rule>` 性のリストについては、の説明を参照してください。

## 正規表現 {#section-4d326507b52544b0960a9a5f303e3fe6}

単純な文字列の一致は非常に基本的なアプリケーションで機能しますが、ほとんどの場合は正規表現が必要です。 正規表現は業界標準ですが、具体的な実装はインスタンスによって異なります。

[パッケージjava.util.regexでは](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) 、画像サービングで使用される具体的な正規表現の実装を説明しています。

## 取り込んだサブ文字列 {#section-8057cd65d48949ffb6a50e929bd3688b}

複雑なURLの変更を容易にするために、サブ文字列を丸括弧(...)で囲むことで、式内でサブ文字列を取り込むことができます。 取り込まれたサブ文字列には、先頭の括弧の位置に従って1から順に番号が付けられます。 取り込んだサブ文字列は、を使用して置換に挿入で *`$n`*&#x200B;きます。は、 *`n`* 取り込んだサブ文字列のシーケンス番号です。

## ルールセットファイルの管理 {#section-e8ce976b56404c009496426fd334d23d}

カタログ属性を持つ各マテリアルカタログには、1つのルールセットファイルを添付できま `attribute::RuleSetFile`す。 ルールセットファイルはいつでも編集できますが、Image Serverは、関連するマテリアルカタログが再読み込みされた場合にのみ変更を認識します。 これは、プラットフォームサーバーが起動または再起動された場合、および（ファイルのサフィックスが付いた）プライマリカタログファイルが変更または「タッチ」された場合（ファイルの日付を変更する場合）に発生します。 [!DNL .ini]

## 例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

ルールセットの例は、画像サービングのドキュメントの画像カタログ参照の対応する節に記載されています。

## 関連項目 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[パッケージjava.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
