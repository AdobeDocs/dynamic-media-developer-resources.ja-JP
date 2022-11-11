---
description: 画像サービングは、正規表現の一致と置き換えルールに基づく、単純な要求前処理メカニズムをサポートします。
solution: Experience Manager
title: ルールセットのリファレンス
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dfbb5f5e-d75a-496a-8b97-f102ad1a34d5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '798'
ht-degree: 0%

---

# ルールセットのリファレンス{#rule-set-reference}

画像サービングは、正規表現の一致と置き換えルールに基づく、単純な要求前処理メカニズムをサポートします。

一連の前処理ルール (*ルールセット*) は、画像カタログまたはデフォルトのカタログにアタッチできます。 デフォルトカタログのルールは、リクエストが特定のメイン画像カタログを識別しない場合にのみ適用されます。

リクエストの前処理ルールでは、リクエストが [!DNL Platform Server]パスの操作、コマンドの追加、コマンド値の変更、テンプレートまたはマクロの適用を含むのパーサー。 また、ルールは、要求の難読化、ウォーターマークなど、通常はカタログ属性でのみ制御される特定のセキュリティ機能を設定および上書きし、特定のクライアント IP アドレスに対するサービスを制限する場合にも使用できます。

ルールセットは、XML ドキュメントファイルとして保存されます。 ルールセットファイルの相対パスまたは絶対パスは、 `attribute::RuleSetFile`.

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

この `<?xml>` および `<ruleset>` 要素は、実際のルールが定義されていない場合でも、常に有効なルールセット XML ファイルで必要です。

1 `<ruleset>` 任意の数のを含む要素 `<rule>` 要素を使用できます。

前処理ルールファイルの内容では、大文字と小文字が区別されます。

## ルールセットの検証 {#section-d8d101a0b4d74580835e37d128d05567}

のコピー [!DNL RuleSet.xsd] は catalog フォルダーに提供され、ruleset ファイルをに登録する前に検証するために使用する必要があります [!DNL catalog.ini] ファイル。 画像サービングでは、 [!DNL RuleSet.xsd] を参照してください。

## URL の前処理 {#section-2c09a2d79ada46b994857c6a7fb4c13a}

他の処理がおこなわれる前に、受信 HTTP リクエストが部分的に解析され、適用する画像カタログが決定されます。 カタログを特定すると、選択したカタログ（特定のカタログが識別されなかった場合はデフォルトのカタログ）のルールセットが適用されます。

この `<rule>` 要素は、 `<expression>` 要素 ( *`expression`*) をクリックします。

次の場合、 `<rule>` が一致する場合、オプション *`substitution`* が適用され、変更されたリクエスト文字列が通常の処理のためにサーバーのリクエストパーサーに渡されます。

一致が見つからなかった場合、 `<ruleset>` に達した場合、リクエストは変更されずにパーサーに渡されます。

## OnMatch 属性 {#section-ed952fa55d99422db0ee68a2b9d395d3}

デフォルトの動作は `OnMatch` の属性 `<rule>` 要素。 `OnMatch` は次のように設定されます。 `break` （デフォルト）、 `continue`または `error`.

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
   <td> <p>置き換えが適用され、次のルールで処理が続行されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> &lt;rule OnMatch="error"&gt; </span> </p> </td> 
   <td> <p>ルール処理は直ちに終了し、「リクエスト拒否」応答ステータスがクライアントに返されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## カタログ属性の上書き {#section-3f1e33a65c5346d1b4a69958c61432f3}

この `rule` 要素では、ルールが正しく一致した場合に対応するカタログ属性を上書きする属性をオプションで定義できます。 一致した複数のルールが同じ属性を設定する場合は、最後のルールが優先されます。 詳しくは、 [ルール](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-rule-rule.md) 要素を参照してください。

## 正規表現 {#section-3f77bb9a265147b38c645f63ab1bad8b}

単純な文字列の照合は非常に基本的なアプリケーションで機能しますが、ほとんどのインスタンスでは正規表現が必要です。 正規表現は業界標準ですが、具体的な実装はインスタンスによって異なります。

[ [!DNL package java.util.regex] ](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/) は、画像サービングで使用される特定の正規表現の実装について説明します。

## 取り込まれたサブ文字列 {#section-066e659406d5403599cd26ae35e80d68}

複雑な URL の変更を容易にするために、サブ文字列を括弧 (...) で囲むことで、式にサブ文字列を取り込むことができます。 取り込まれたサブ文字列には、先頭の括弧の位置に従って 1 から順に番号が付けられます。 取得したサブ文字列は、 ` $ *`n`*`で、 *`n`* は、取り込まれた部分文字列のシーケンス番号です。

## ルールセットファイルの管理 {#section-0598a608e4044bb4805fe93ceebe10a9}

カタログ属性を使用して、各画像カタログに 1 つのルールセットファイルを添付できます `attribute::RuleSetFile`. ルールセットファイルはいつでも編集できますが、関連する画像カタログが再読み込みされた場合にのみ、Image Server は変更を認識します。 この再読み込みは、プラットフォームサーバーが起動または再起動されたときや、 [!DNL .ini] ファイルのサフィックス。ファイルの日付を変更するには「touched」を指定します。

## 例 {#section-aa769437d967459299b83a4bf34fe924}

**例 A.** 画像名に「 」というサフィックスが付いている場合に画質設定を増やすルールを定義する [!DNL _hg]&quot;:

```
<rule> 
   <expression>(?i)_hg$</expression> 
   <substitution>\?&amp;qlt=95,1&amp;resmode=bicub</substitution> 
</rule>
```

ルール式は、「 [!DNL _hg]」と呼ばれ、URL 文字列の末尾に配置されます。 サフィックスは、画質設定を変更する、指定されたクエリ文字列に置き換えられます。 なお、 `?` 置換文字列の文字は正規表現の特殊文字なので、エスケープされます。

>[!NOTE]
>
>アンパサンド文字に必要なエンコーディング。 または、置換文字列を CDATA ブロックで囲むこともできます。

`<substitution><![CDATA[&qlt=95,1&resmode=bicub]]></substitution>`

**例 B.** 特定の Web アプリケーションでは、クエリ文字列を許可していません。 末尾のパス要素を変換するルールを定義する `small`, `medium`または `large` 残りのパスを画像名として使用して、テンプレートに追加します。 例： `myCat/myImage/small` 次の値に変換 `myCat/smallTemplate?src=myCat/myImage`.

サブ文字列を使用して、リクエストを再構築できます。

```
<rule> 
   <expression>([^/]+)/(small|medium|large)$</expression> 
   <substitution>$2Template?src=sample/$1</substitution> 
</rule>
```

## 関連項目 {#section-9b748e7c5cff4759a70f96657bd43352}

[package java.util.regex](https://www2.cs.duke.edu/csed/java/jdk1.4.2/docs/api/)
