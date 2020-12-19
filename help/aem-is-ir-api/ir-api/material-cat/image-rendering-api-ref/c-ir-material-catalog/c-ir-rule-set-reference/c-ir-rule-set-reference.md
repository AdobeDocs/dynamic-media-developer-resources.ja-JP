---
description: 画像レンダリングでは、正規式の一致と置換ルールに基づく単純なリクエスト前処理メカニズムがサポートされています。
seo-description: 画像レンダリングでは、正規式の一致と置換ルールに基づく単純なリクエスト前処理メカニズムがサポートされています。
seo-title: ルールセットの参照
solution: Experience Manager
title: ルールセットの参照
topic: Scene7 Image Serving - Image Rendering API
uuid: aeec7597-4d23-4cf8-8bdc-3a133152eadb
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '654'
ht-degree: 0%

---


# ルールセットの参照{#rule-set-reference}

画像レンダリングでは、正規式の一致と置換ルールに基づく単純なリクエスト前処理メカニズムがサポートされています。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

事前処理ルールのコレクション（*ルールセット*）は、マテリアルカタログまたはデフォルトのカタログにアタッチできます。 デフォルトカタログのルールは、リクエストが特定の材料カタログをアタッチしない場合にのみ適用されます。

リクエストの事前処理ルールでは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、リクエストがサーバーのリクエストパーサーによって処理される前に、リクエストのパスとクエリの部分を変更できます。 ルールは、一部のカタログ属性の設定と上書き、サービスを特定のクライアントIPアドレスに制限する場合にも使用できます。

ルールセットは、XMLドキュメントファイルとして保存されます。 ルールセットファイルの相対パスまたは絶対パスを`attribute::RuleSetFile`で指定する必要があります。

## 一般的な構造{#section-74faaee27fc543a2ab4a306f3a03674e}

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

有効なルールセットXMLファイルでは、実際のルールが定義されていない場合でも、`<?xml>`、`<!DOCTYPE>`、`<ruleset>`の要素が必ず必要です。

任意の数の`<rule>`要素を含む`<ruleset>`要素を1つだけ使用できます。

前処理ルールファイルの内容は、大文字と小文字が区別されます。

## URLの前処理{#section-737a38d1b8c746f995e64fa6cfbcec87}

他の処理の前に、着信HTTPリクエストが部分的に解析され、適用する材料カタログが決定されます。 カタログが識別されると、選択したカタログ（または特定のカタログが識別されなかった場合はデフォルトのカタログ）のルールセットが適用されます。

`<rule>`要素は、`<expression>`要素(*`expression`*)の内容と一致するように指定された順に検索されます。

`<rule>`が一致した場合は、オプションの&#x200B;*`substitution`*&#x200B;が適用され、変更された要求文字列がサーバーの要求パーサーに渡され、通常の処理が行われます。

`<ruleset>`の終わりに達したときに一致が見つからなかった場合、リクエストは変更されずにパーサーに渡されます。

## OnMatch属性{#section-7a8ad3597780486985af5e9a3b1c7b56}

デフォルトの動作は、`<rule>`要素の`OnMatch`属性を使用して変更できます。 `OnMatch` は、 `break` （デフォルト）、 `continue`または  `error.`

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
   <td colname="col2"> <p>ルールの処理は、このルールの置き換えが適用された直後に終了します。 初期設定. </p> </td> 
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

## カタログ属性の上書き{#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` の要素では、ルールが適切に一致し、設定された場合に、対応するカタログ属性を上書きする属性を任意 `OnMatch="break"` で定義できます。`OnMatch="continue"`が設定されている場合、属性は適用されません。 ルールで制御できる属性のリストについては、`<rule>`の説明を参照してください。

## 正規式{#section-4d326507b52544b0960a9a5f303e3fe6}

単純な文字列の一致は非常に基本的なアプリケーションで機能しますが、通常の式は必須です。 正規式は業界標準ですが、具体的な実装はインスタンスによって異なります。

[パッケージjava.util.](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) regexでは、画像サービングで使用される具体的な正規式の実装を説明します。

## 捕捉したサブ文字列{#section-8057cd65d48949ffb6a50e929bd3688b}

複雑なURLの変更を容易にするために、サブ文字列を丸括弧(...)で囲むことで、式内でサブ文字列を取り込むことができます。 取り込んだサブ文字列には、先頭の括弧の位置に従って、1から順に連番が付けられます。 *`$n`*&#x200B;を使用して、捕捉したサブ文字列を置換に挿入できます。*`n`*&#x200B;は、捕捉したサブ文字列のシーケンス番号です。

## ルールセットファイルの管理{#section-e8ce976b56404c009496426fd334d23d}

カタログ属性`attribute::RuleSetFile`を持つ各マテリアルカタログには、1つのルールセットファイルをアタッチできます。 ルールセットファイルはいつでも編集できますが、Image Serverは、関連付けられたマテリアルカタログが再読み込みされた場合にのみ変更を認識します。 これは、プラットフォームサーバーが起動または再起動されたときや、（[!DNL .ini]ファイルのサフィックスを持つ）プライマリカタログファイルが変更されたり、（ファイルの日付を変更するために）「タッチ」されたときに起こります。

## 例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

ルールセットの例は、画像サービングのドキュメントの画像カタログ参照の対応する節に記載されています。

## 関連項目 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[パッケージjava.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
