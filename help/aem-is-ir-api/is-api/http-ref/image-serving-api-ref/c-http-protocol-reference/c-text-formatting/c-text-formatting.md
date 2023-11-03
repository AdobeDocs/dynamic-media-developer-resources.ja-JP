---
description: 画像サービングには、text=および textPs=コマンドを使用してアクセスできる、テキストのレンダリングに対するいくつかの代替手段が用意されています。
solution: Experience Manager
title: テキストの書式設定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 7%

---

# テキストの書式設定{#text-formatting}

画像サービングには、text=および textPs=コマンドを使用してアクセスできる、テキストのレンダリングに対するいくつかの代替手段が用意されています。

`textPs=` は、Adobe PhotoshopとIllustratorでレンダリングされるテキストとの高い類似性を提供します。 `text=` は、Windows Wordpad でレンダリングされたテキストと適切に互換性があります。

>[!NOTE]
>
>他の場所で挙げられている違いに加えて、 `text=` と比較すると、レンダリングされたテキストに微妙な違いが生じます。 `textPs=`. たとえば、下線の厚さと位置が同じではなく、合成された斜体が少し異なる角度でレンダリングされます。 テキストが使用可能なスペースに収まらない場合は、 `text=` 最後の行を部分的に切り抜くことができます。 `textPs=` は、完全な線のみをレンダリングします。

すべてのテキストコマンドは、RTF（リッチテキストフォーマット）仕様のサブセットに基づいて、書式付きテキストを受け付けます。 各テキストレイヤーは、異なるテキストコマンドを指定できます。

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
   <td> <p>任意の図形にテキストを流し込む </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>任意のパスに沿ったテキストの流れ </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>継ぎ手のコピー </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> [ 継手をコピー ] <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>テキストボックスの余白 </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落全体の位置合わせ </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>最終行の位置合わせ </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落インデント </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>オールキャップスおよびスモールキャップステキスト </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>画像サービングのカラー </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\*\iscorortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>複数のアンチエイリアシングモード </p> </td> 
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
   <td> <p>テキストに合わせてレイヤーを自動サイズ変更 </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>text=、textId=、size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK サポート </p> </td> 
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
   <td> <p>レイヤーに合わせてテキストを自動的に拡大・縮小（解像度を変更） </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF に準拠した文字列は、手動で組み立てるか、RTF ファイルを保存できるテキストエディタやワードプロセッサで目的のテキストをフォーマットすることで組み立てることができます。 次に、RTF ファイルをプレーンテキストエディタで開き、リクエスト URL にコピーされたファイルの関連する生の RTF コンテンツを作成します。

一部のワードプロセッサーでは、かなり大きなファイルが生成され、Dynamic Media Image Serving で使用されない実質的なプリアンブルが含まれます。 未使用の RTF 要素は、文字列をテキストコマンドに渡す前に、文字列から削除することをお勧めします。

UTF-8 および ISO 規格に基づく言語エンコーディングは、標準の RTF 文字エンコーディングメカニズムの代わりに、RTF 文字列でサポートされます。 これにより、RTF エンコーディングを知らなくても、アプリケーションは英語以外のテキストをサーバに送信できます。

文字列を http 経由で送信する場合は、HTTP 準拠でないすべての文字を適切にエスケープする必要があります。 文字列を `catalog::Modifiers` 画像カタログレコードのフィールド。 次を含む制御文字 `<CR>`, `<LF>`、および `<TAB>` は常に削除する必要があります。

画像サービングテキストエンジンは、リッチテキスト形式 (RTF) 仕様バージョン 1.6 で定義されたコマンドのサブセットを解釈します。このサブセットは、フォント/文字の書式設定、単純な段落書式設定、および国際フォントと文字セットのサポートに焦点を当てています。 現時点では、スタイルシートやテーブルなど、より高度な書式設定構成はサポートされていません。

RTF エンコードされたテキスト文字列を手動で作成する場合は、Microsoftが公開するリッチテキスト形式 (RTF) 仕様に関する知識が必要です。

* [フォントの処理](r-font-handling.md)
* [カラー処理](r-color-handling.md)
* [継ぎ手のコピー](r-copy-fitting.md)
* [テキストレイヤー](r-text-layers.md)
* [テキストの配置](r-text-positioning.md)
* [予約文字](r-reserved-characters.md)
* [サポートされる RTF コマンドとキーワード](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF エンコードの例](r-rtf-encoding-examples.md)
