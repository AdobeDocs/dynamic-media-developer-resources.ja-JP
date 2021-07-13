---
description: 画像サービングには、text=およびtextPs=コマンドを使用してアクセスできる、テキストのレンダリングに対する代替手段がいくつか用意されています。
solution: Experience Manager
title: テキストの書式設定
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '562'
ht-degree: 7%

---

# テキストの書式設定{#text-formatting}

画像サービングには、text=およびtextPs=コマンドを使用してアクセスできる、テキストのレンダリングに対する代替手段がいくつか用意されています。

`textPs=` は、Adobe PhotoshopやIllustratorでレンダリングされるテキストとの高い類似性を提供します。`text=` は、Windows Wordpadでレンダリングされたテキストと適切に互換性があります。

>[!NOTE]
>
>`text=`は、他の場所にリストされている違いに加え、`textPs=`と比較した場合に、レンダリングされたテキストに微妙な違いを生み出します。 例えば、下線の太さと位置が同じではなく、合成された斜体が少し異なる角度でレンダリングされます。 テキストが使用可能な領域に収まらない場合、`text=`は最後の行を部分的に切り抜くのに対して、`textPs=`は完全な行のみをレンダリングします。

すべてのテキストコマンドは、RTF（リッチテキストフォーマット）仕様のサブセットに基づいて書式化されたテキストを受け付けます。 各テキストレイヤーは、異なるテキストコマンドを指定できます。

次の表に、各テキストコマンドで使用できる主な機能を示します。

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 機能</b> </th> 
   <th class="entry"> <b> テキスト=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> 関連項目</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> Adobe Photoshop互換 </p> </td> 
   <td> <p> no </p> </td> 
   <td> <p> 制限 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>任意の図形にテキストを流す </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>任意のパスに沿ったテキストのフロー </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>継ぎ手のコピー </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> コピー — 継手 <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>テキストボックスの余白 </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落全体の位置揃え </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>最後の行揃え </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落インデント </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\fi、\li、\ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>すべて大文字と小文字のテキスト </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>画像サービングのカラー </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>複数のアンチエイリアスモード </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>上下/右左のテキストフロー </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Photofont®のサポート </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> フォント処理 </td> 
  </tr> 
  <tr> 
   <td> <p>テキストに合わせてレイヤーを自動サイズ設定 </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>text=、textId=、size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYKのサポート </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>右から左の文字フロー </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>ワードラップを無効にする </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>レイヤーに合わせてテキストを自動拡大/縮小（解像度を変更） </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF準拠の文字列は、手動で組み立てるか、RTFファイルを保存可能なテキストエディタやワードプロセッサで目的のテキストをフォーマットすることで組み立てることができます。 次に、RTFファイルをプレーンテキストエディターで開き、リクエストURLにコピーされたファイルの関連する生のRTFコンテンツを作成します。

一部のワードプロセッサーでは、大きなファイルが生成され、Dynamic Media Image Servingで使用されない実質的なプリアンブルが含まれます。 未使用のRTF要素を文字列から削除してから、文字列をテキストコマンドに渡すことをお勧めします。

UTF-8およびISO標準に基づく言語エンコーディングは、標準のRTF文字エンコーディングメカニズムの代わりに、RTF文字列でサポートされます。 これにより、アプリケーションはRTFエンコーディングを知らなくても英語以外のテキストをサーバーに送信できます。

文字列をhttp経由で送信する場合は、HTTPに準拠していないすべての文字を適切にエスケープする必要があります。 画像カタログレコードの`catalog::Modifiers`フィールドに文字列を組み込む場合は、「=」、「&amp;」および「%」のみをエスケープする必要があります。 `<CR>`、`<LF>`、`<TAB>`などの制御文字は、常に削除する必要があります。

画像サービングテキストエンジンは、リッチテキストフォーマット(RTF)仕様1.6で定義されたコマンドのサブセットを解釈します。このサブセットは、フォント/文字の書式設定、単純な段落書式設定、国際フォントと文字セットのサポートに重点を置いています。 現時点では、スタイルシートやテーブルなど、より高度な書式設定構成はサポートされていません。

RTFエンコードされたテキスト文字列を手動で作成する場合は、Microsoftが発行したリッチテキスト形式(RTF)仕様に精通する必要があります。

* [フォントの処理](r-font-handling.md)
* [カラー処理](r-color-handling.md)
* [継ぎ手のコピー](r-copy-fitting.md)
* [テキストレイヤー](r-text-layers.md)
* [テキストの配置](r-text-positioning.md)
* [予約文字](r-reserved-characters.md)
* [サポートされるRTFコマンドとキーワード](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTFエンコーディングの例](r-rtf-encoding-examples.md)
