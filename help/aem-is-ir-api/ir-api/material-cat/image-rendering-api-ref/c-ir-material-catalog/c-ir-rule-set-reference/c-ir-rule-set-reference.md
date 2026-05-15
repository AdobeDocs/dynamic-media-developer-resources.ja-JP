---
description: 画像レンダリングは、正規表現の一致と置換ルールに基づくシンプルなリクエスト前処理メカニズムをサポートしています。
solution: Experience Manager
title: ルールセット参照
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
TQID: 'https://experienceleague.adobe.com/HxgWcboIyA2RYuXbHMKaUiRQFL8IDNKegdOqMgz2plE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 642
ht-degree: 0%

---

# ルールセット参照{#rule-set-reference}

画像レンダリングは、正規表現の一致と置換ルールに基づくシンプルなリクエスト前処理メカニズムをサポートしています。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

前処理ルールのコレクション（*ルールセット*）は、マテリアルカタログまたはデフォルトカタログに添付できます。 デフォルトカタログのルールは、リクエストが特定のマテリアルカタログを添付しない場合にのみ適用されます。

リクエスト前処理ルールは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、サーバーのリクエストパーサーによって処理される前に、リクエストのパスとクエリ部分を変更できます。 また、一部のカタログ属性の設定や上書き、特定のクライアント IP アドレスへのサービスの制限にもルールを使用できます。

ルールセットは、XML ドキュメントファイルとして保存されます。 ルール セット ファイルの相対パスまたは絶対パスを`attribute::RuleSetFile`で指定する必要があります。

## 一般構造 {#section-74faaee27fc543a2ab4a306f3a03674e}

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

実際のルールが定義されていない場合でも、有効なルールセット XML ファイルでは、`<?xml>`、`<!DOCTYPE>`および`<ruleset>`要素が常に必要です。

任意の数の`<rule>`要素を含む1つの`<ruleset>`要素を使用できます。

前処理ルールファイルの内容では、大文字と小文字が区別されます。

## URLの事前処理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

他の処理の前に、受信HTTP リクエストが部分的に解析され、どのマテリアルカタログを適用するかを決定します。 カタログが識別されると、選択したカタログのルールセット（または特定のカタログが識別されていない場合はデフォルトのカタログ）が適用されます。

`<rule>`要素は、`<expression>`要素（*`expression`*）の内容と一致するように指定された順序で検索されます。

`<rule>`が一致する場合、オプションの&#x200B;*`substitution`*&#x200B;が適用され、変更されたリクエスト文字列が通常の処理のためにサーバーのリクエストパーサーに渡されます。

`<ruleset>`の末尾に到達したときに一致が成功しなかった場合、リクエストは変更なしでパーサーに渡されます。

## OnMatch属性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

デフォルトの動作は、`<rule>`要素の`OnMatch`属性で変更できます。 `OnMatch`は`break` （デフォルト）、`continue`、または`error.`に設定できます

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
   <td colname="col2"> <p>ルール処理は、このルールの代用が適用された直後に終了します。 デフォルト： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>置換が適用され、処理は次のルールで続行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>ルール処理は直ちに終了し、「リクエスト拒否」応答ステータスがクライアントに返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## カタログ属性の上書き {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>`要素は、ルールが正常に一致し、`OnMatch="break"`が設定されたときに、対応するカタログ属性を上書きする属性をオプションで定義できます。 `OnMatch="continue"`が設定されている場合、属性は適用されません。 ルールで制御できる属性のリストについては、`<rule>`の説明を参照してください。

## 正規表現 {#section-4d326507b52544b0960a9a5f303e3fe6}

単純な文字列マッチングは、非常に基本的なアプリケーションで機能しますが、ほとんどの場合、正規表現が必要です。 正規表現は業界標準ですが、具体的な実装はインスタンスによって異なります。

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)は、Image Servingで使用される特定の正規表現の実装について説明します。

## キャプチャされたサブストリング {#section-8057cd65d48949ffb6a50e929bd3688b}

複雑なURLの変更を容易にするために、サブストリングを括弧（。..）で囲むことで、エクスプレッションにサブストリングを取り込むことができます。 キャプチャされたサブストリングには、先頭の括弧の位置に従って、1から始まる番号が付けられます。 キャプチャされたサブストリングは、*`$n`*&#x200B;を使用して置換に挿入できます。ここで、*`n`*&#x200B;はキャプチャされたサブストリングのシーケンス番号です。

## ルールセットファイルの管理 {#section-e8ce976b56404c009496426fd334d23d}

1つのルール セット ファイルを、カタログ属性`attribute::RuleSetFile`を持つ各マテリアル カタログに添付できます。 ルールセットファイルはいつでも編集できますが、関連するマテリアルカタログが再ロードされた場合にのみ、画像サーバーは変更を認識します。 これは、[!DNL Platform Server]が開始または再起動され、プライマリカタログファイル（[!DNL .ini] ファイルのサフィックスを持つ）が変更または「タッチ」（ファイル日付を変更）されるたびに発生します。

## 例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

ルールセットの例は、画像サービングドキュメントの画像カタログリファレンスの対応するセクションに記載されています。

## 関連項目 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[パッケージ java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
