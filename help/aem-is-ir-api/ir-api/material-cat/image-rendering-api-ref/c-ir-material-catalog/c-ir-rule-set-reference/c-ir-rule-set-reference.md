---
description: 画像レンダリングは、正規表現の一致と置き換えルールに基づく、単純なリクエストの前処理メカニズムをサポートしています。
solution: Experience Manager
title: ルールセットのリファレンス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 194600d0-72d9-47fb-8525-598beb2ce17d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# ルールセットのリファレンス{#rule-set-reference}

画像レンダリングは、正規表現の一致と置き換えルールに基づく、単純なリクエストの前処理メカニズムをサポートしています。

<!--<a id="section_F44601A65CE1451EAD0A449C66B773CC"></a>-->

一連の前処理ルール (*ルールセット*) は、マテリアルカタログまたは既定のカタログにアタッチできます。 既定のカタログのルールは、要求が特定の素材カタログをアタッチしない場合にのみ適用されます。

リクエストの前処理ルールは、パスの操作、コマンドの追加、コマンド値の変更、テンプレートやマクロの適用など、リクエストのパスとクエリの部分を、サーバーのリクエストパーサーによって処理される前に変更できます。 ルールは、一部のカタログ属性を設定および上書きする場合や、サービスを特定のクライアント IP アドレスに制限する場合にも使用できます。

ルールセットは、XML ドキュメントファイルとして保存されます。 ルールセットファイルの相対パスまたは絶対パスは、 `attribute::RuleSetFile`.

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

この `<?xml>`, `<!DOCTYPE>` および `<ruleset>` 要素は、実際のルールが定義されていない場合でも、常に有効なルールセット XML ファイルで必要です。

1 `<ruleset>` 任意の数のを含む要素 `<rule>` 要素を使用できます。

前処理ルールファイルの内容では、大文字と小文字が区別されます。

## URL の前処理 {#section-737a38d1b8c746f995e64fa6cfbcec87}

他の処理がおこなわれる前に、受信 HTTP リクエストが部分的に解析されて、適用する材料カタログが決定されます。 カタログを特定すると、選択したカタログ（特定のカタログが識別されなかった場合はデフォルトのカタログ）のルールセットが適用されます。

この `<rule>` 要素は、 `<expression>` 要素 ( *`expression`*) をクリックします。

次の場合、 `<rule>` が一致する場合、オプション *`substitution`* が適用され、変更されたリクエスト文字列が通常の処理のためにサーバーのリクエストパーサーに渡されます。

一致が見つからなかった場合、 `<ruleset>` に達した場合、リクエストは変更されずにパーサーに渡されます。

## OnMatch 属性 {#section-7a8ad3597780486985af5e9a3b1c7b56}

デフォルトの動作は `OnMatch` の属性 `<rule>` 要素。 `OnMatch` は次のように設定されます。 `break` （デフォルト）、 `continue`または `error.`

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
   <td colname="col2"> <p>置き換えが適用され、次のルールで処理が続行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> &lt;rule OnMatch="error"&gt;</span> </p> </td> 
   <td colname="col2"> <p>ルール処理は直ちに終了し、「リクエスト拒否」応答ステータスがクライアントに返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## カタログ属性の上書き {#section-1f59ce84234f4576ba8473b0e6ba22ee}

`<rule>` 要素では、ルールが正常に一致し、 `OnMatch="break"` が設定されている。 次の場合、属性は適用されません。 `OnMatch="continue"` が設定されている。 詳しくは、 `<rule>` ルールで制御できる属性のリスト。

## 正規表現 {#section-4d326507b52544b0960a9a5f303e3fe6}

単純な文字列の照合は非常に基本的なアプリケーションで機能しますが、ほとんどのインスタンスでは正規表現が必要です。 正規表現は業界標準ですが、具体的な実装はインスタンスによって異なります。

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) は、画像サービングで使用される特定の正規表現の実装について説明します。

## 取り込まれたサブ文字列 {#section-8057cd65d48949ffb6a50e929bd3688b}

複雑な URL の変更を容易にするために、サブ文字列を括弧 (...) で囲むことで、式にサブ文字列を取り込むことができます。 取り込まれたサブ文字列には、先頭の括弧の位置に従って 1 から順に番号が付けられます。 取得したサブ文字列は、 *`$n`*&#x200B;で、 *`n`* は、取り込まれた部分文字列のシーケンス番号です。

## ルールセットファイルの管理 {#section-e8ce976b56404c009496426fd334d23d}

カタログ属性を持つ各マテリアルカタログに 1 つのルールセットファイルをアタッチできます `attribute::RuleSetFile`. ルールセットファイルはいつでも編集できますが、イメージサーバは、関連するマテリアルカタログが再ロードされた場合にのみ変更を認識します。 これは、 [!DNL Platform Server] が起動または再起動されたときと、( [!DNL .ini] ファイルのサフィックス ) が変更または「touched」（ファイルの日付を変更する場合）になります。

## 例 {#section-c4142a41f5cd4ff799a72fbc130c3700}

Ruleset の例は、画像サービングドキュメントの画像カタログ参照の対応する節に記載されています。

## 関連項目 {#section-cdaacf84f92c4bffbb4b76197b4e531a}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
