---
description: 画像レンダリングは、正規表現の一致および置換ルールに基づく単純なリクエスト前処理メカニズムをサポートしています。
solution: Experience Manager
title: ルールセットの参照
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 0%

---

# ルールセットの参照{#rule-set-reference}

画像レンダリングは、正規表現の一致および置換ルールに基づく単純なリクエスト前処理メカニズムをサポートしています。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

前処理ルールのコレクション（*ルール セット*）は、材料カタログまたはデフォルトのカタログに添付できます。 既定のカタログのルールは、要求が特定の材料カタログを添付しない場合にのみ適用されます。

要求の前処理ルールでは、サーバーの要求パーサーで処理される前に、要求のパスおよびクエリ部分を変更できます（パスの操作、コマンドの追加、コマンド値の変更、テンプレートまたはマクロの適用など）。 また、一部のカタログ属性を設定および上書きしたり、サービスを特定のクライアント IP アドレスに制限したりするために、ルールを使用することもできます。

ルールセットは XML ドキュメントファイルとして保存されます。 ルールセットファイルの相対パスまたは絶対パスを `attribute::RuleSetFile` で指定する必要があります。

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

実際のルールが定義されていない場合でも、有効なルールセット XML ファイルでは `<?xml>`、`<!DOCTYPE>` および `<ruleset>` 要素が常に必要です。

任意の数の `<ruleset>` 要素を含む 1 つの `<rule>` 要素を使用できます。

前処理ルールファイルの内容では、大文字と小文字が区別されます。

## URL の前処理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

他の処理を行う前に、受信した HTTP リクエストを部分的に解析し、どの材料カタログを適用するかを決定します。 カタログが識別されると、選択したカタログ（特定のカタログが識別されていない場合はデフォルトのカタログ）のルールセットが適用されます。

`<rule>` 要素は、指定された順序で検索されて、`<expression>` 要素のコンテンツ（*`expression`*）と一致します。

`<rule>` が一致する場合、オプションの *`substitution`* が適用され、変更されたリクエスト文字列が通常の処理のためにサーバーのリクエストパーサーに渡されます。

`<ruleset>` の終わりに達してもマッチに成功しなかった場合、リクエストは変更されずにパーサに渡されます。

## Onmatch 属性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

デフォルトの動作は、`OnMatch` 要素の `<rule>` 属性で変更できます。 `OnMatch` は `break` （デフォルト）、`continue`、`error.` のいずれかに設定できます

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
   <td colname="col2"> <p>ルールの処理は、このルールの代用が適用された直後に終了します。 デフォルト。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>置換が適用され、処理は次のルールに進みます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>ルールの処理は直ちに終了し、「リクエストが拒否されました」応答ステータスがクライアントに返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## カタログ属性の上書き {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 要素では、ルールが正常に一致し、`OnMatch="break"` が設定された場合に、対応するカタログ属性を上書きする属性をオプションで定義できます。 `OnMatch="continue"` が設定されている場合、属性は適用されません。 ルールで制御できる属性のリストについては、`<rule>` の説明を参照してください。

## 正規表現 {#section-4d326507b52544b0960a9a5f303e3fe6}

単純な文字列のマッチングは非常に基本的なアプリケーションで機能しますが、ほとんどの場合は正規表現が必要です。 正規表現は業界標準ですが、実装はインスタンスによって異なります。

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) は、画像サービングで使用される特定の正規表現実装について説明します。

## キャプチャされた部分文字列 {#section-8057cd65d48949ffb6a50e929bd3688b}

複雑な URL 変更を容易にするために、部分文字列を括弧（...）で囲んで式に取り込むことができます。 取り込まれた部分文字列は、先頭の括弧の位置に従って、1 から順に番号が付けられます。 取得された部分文字列は、*`$n`* を使用した置換に挿入できます。ここで、*`n`* は、取得された部分文字列のシーケンス番号です。

## 規則セットファイルの管理 {#section-e8ce976b56404c009496426fd334d23d}

カタログ属性 `attribute::RuleSetFile` を使用して、各材料カタログに 1 つのルール セット ファイルをアタッチできます。 ルール セット ファイルはいつでも編集できますが、Image Server は、関連付けられたマテリアル カタログが再ロードされたときにのみ変更を認識します。 これは、[!DNL Platform Server] ージが開始または再起動されたときや、プライマリカタログファイル（ファイルのサフィックスが [!DNL .ini] い）が変更または「タッチ」（ファイルの日付を変更するため）されるたびに発生します。

## 例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

ルールセットの例については、画像サービングドキュメントの画像カタログ参照の対応するセクションに記載されています。

## 関連項目 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
