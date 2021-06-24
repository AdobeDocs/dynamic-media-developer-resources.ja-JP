---
description: 画像レンダリングは、正規表現の一致と置換ルールに基づく、シンプルなリクエストの前処理メカニズムをサポートしています。
solution: Experience Manager
title: ルールセットのリファレンス
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '639'
ht-degree: 0%

---

# ルールセットのリファレンス{#rule-set-reference}

画像レンダリングは、正規表現の一致と置換ルールに基づく、シンプルなリクエストの前処理メカニズムをサポートしています。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

前処理ルールのコレクション（*ルールセット*）は、マテリアルカタログまたは既定のカタログに添付できます。 既定のカタログのルールは、要求が特定の材料カタログをアタッチしない場合にのみ適用されます。

リクエストの前処理ルールでは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、リクエストのパスとクエリの部分を、サーバーのリクエストパーサーによって処理される前に変更できます。 ルールは、一部のカタログ属性を設定および上書きする場合や、サービスを特定のクライアントIPアドレスに制限する場合にも使用できます。

ルールセットは、XMLドキュメントファイルとして保存されます。 ルールセットファイルの相対パスまたは絶対パスを`attribute::RuleSetFile`で指定する必要があります。

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

`<?xml>`、`<!DOCTYPE>`および`<ruleset>`要素は、実際のルールが定義されていなくても、有効なルールセットXMLファイルで常に必要です。

任意の数の`<rule>`要素を含む`<ruleset>`要素を1つ使用できます。

前処理ルールファイルの内容では大文字と小文字が区別されます。

## URLの前処理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

その他の処理の前に、受信HTTPリクエストが部分的に解析され、適用する材料カタログが決定されます。 カタログが識別されると、選択したカタログ（特定のカタログが識別されなかった場合はデフォルトのカタログ）のルールセットが適用されます。

`<rule>`要素は、`<expression>`要素(*`expression`*)の内容と一致するように指定された順序で検索されます。

`<rule>`が一致する場合は、オプションの&#x200B;*`substitution`*&#x200B;が適用され、変更されたリクエスト文字列が通常の処理のためにサーバーのリクエストパーサーに渡されます。

`<ruleset>`の終わりに達しても一致が見つからない場合、リクエストは変更されずにパーサーに渡されます。

## OnMatch属性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

デフォルトの動作は、`<rule>`要素の`OnMatch`属性で変更できます。 `OnMatch` は（デフォルト） `break` 、または `continue`に設定できます。  `error.`

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
   <td colname="col2"> <p>ルールの処理は、このルールの置換が適用された直後に終了します。 初期設定. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="continue"&gt;</span> </p> </td> 
   <td colname="col2"> <p>置換が適用され、次のルールで処理が続行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>ルールの処理は直ちに終了し、「リクエスト拒否」応答ステータスがクライアントに返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## カタログ属性の上書き {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 要素では、ルールが正しく照合され、設定された場合に、対応するカタログ属性を上書きする属性をオプシ `OnMatch="break"` ョンで定義できます。`OnMatch="continue"`が設定されている場合、属性は適用されません。 ルールで制御できる属性のリストについては、 `<rule>`の説明を参照してください。

## 正規表現 {#section-4d326507b52544b0960a9a5f303e3fe6}

単純な文字列のマッチングは非常に基本的なアプリケーションで機能しますが、ほとんどの場合、正規表現が必要です。 正規表現は業界標準ですが、実装はインスタンスによって異なります。

[package java.util.regexは、画像サービ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) ングで使用される特定の正規表現の実装を示します。

## 取り込まれたサブ文字列 {#section-8057cd65d48949ffb6a50e929bd3688b}

複雑なURLの変更を容易にするために、サブ文字列を括弧(...)で囲むことで、式にサブ文字列を取り込むことができます。 取り込まれたサブ文字列には、先頭の括弧の位置に従って1から順に番号が付けられます。 *`$n`*&#x200B;を使用して、取り込んだサブ文字列を置換に挿入できます。*`n`*&#x200B;は、取り込んだサブ文字列のシーケンス番号です。

## ルールセットファイルの管理 {#section-e8ce976b56404c009496426fd334d23d}

カタログ属性`attribute::RuleSetFile`を使用して、各マテリアルカタログに1つのルールセットファイルをアタッチできます。 ルールセットファイルはいつでも編集できますが、イメージサーバは、関連するマテリアルカタログが再ロードされた場合にのみ変更を認識します。 これは、Platform Serverが起動または再起動されたときや、（[!DNL .ini]ファイルのサフィックスを持つ）プライマリカタログファイルが変更または「touch」（ファイルの日付を変更するため）されたときに常に発生します。

## 例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

ルールセットの例は、画像サービングのドキュメントの画像カタログ参照の対応する節に記載されています。

## 関連項目 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[パッケージjava.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
