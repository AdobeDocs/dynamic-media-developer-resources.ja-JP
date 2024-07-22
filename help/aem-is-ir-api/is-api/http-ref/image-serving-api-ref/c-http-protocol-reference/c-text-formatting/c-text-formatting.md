---
description: 画像サービングには、テキストをレンダリングするためのいくつかの代替手段が用意されており、text=および textPs= コマンドを使用してアクセスできます。
solution: Experience Manager
title: テキストフォーマット
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 6%

---

# テキストフォーマット{#text-formatting}

画像サービングには、テキストをレンダリングするためのいくつかの代替手段が用意されており、text=および textPs= コマンドを使用してアクセスできます。

`textPs=` は、Adobe PhotoshopとIllustratorでレンダリングされるテキストとの高いレベルの類似性を提供します。 `text=` は、Windows ワードパッドで表示されるテキストと適度に互換性があります。

>[!NOTE]
>
>他の場所にリストされている違いに加えて、`text=` は `textPs=` と比較すると、レンダリングされるテキストにわずかな違いがあります。 例えば、アンダーラインの太さと位置は同じではなく、合成された斜体は少し異なる角度でレンダリングされます。 テキストが使用可能なスペースに収まらない場合は、最後の行 `text=` 部分的に切り抜かれる可能性がありますが、`textPs=` は完全な行のみをレンダリングします。

すべてのテキストコマンドは、RTF （Rich Text Format）仕様のサブセットに基づく書式設定されたテキストを受け付けます。 テキストレイヤーごとに異なるテキストコマンドを指定できます。

次の表に、各テキスト コマンドで使用できる主な機能を示します。

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 機能 </b> </th> 
   <th class="entry"> <b> text=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b> 関連項目 </b> </th> 
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
   <td> <p>テキストを任意の形状に流し込む </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>任意のパスに沿ってテキストをフロー設定 </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Copy-fitting </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> Copy-Fitting <p>, <pre>\コピーフィット</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>テキストボックスの余白 </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落全体の行揃え </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>最後の行の位置合わせ </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落のインデント </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\fi, \li, \ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>すべて大文字と小型大文字のテキスト </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\caps, \scaps </p> </td> 
  </tr> 
  <tr> 
   <td> <p>画像サービングカラー </p> </td> 
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
   <td> <p>テキストの上下左右のフロー </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>（Photofont® サポート） </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> フォントの処理 </td> 
  </tr> 
  <tr> 
   <td> <p>テキストに合わせてレイヤーのサイズを自動調整 </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>text=, textId=, size= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>CMYK サポート </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\cmykcolortbl, \*\iscolortbl </p> </td> 
  </tr> 
  <tr> 
   <td> <p>右から左への文字フロー </p> </td> 
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
   <td> <p>レイヤーに合わせてテキストを自動スケール （解像度を変更） </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF 準拠の文字列は、手動で組み立てることも、RTF ファイルを保存できるテキストエディターやワードプロセッサーで目的のテキストを書式設定することもできます。 その後、RTF ファイルをプレーンテキストエディターで開き、関連する生の RTF コンテンツをリクエスト URL にコピーできます。

一部のワードプロセッサーは、かなり大きなファイルを生成します。これには、Dynamic Media画像サービングで使用されない実質的なプリアンブルが含まれています。 文字列をテキストコマンドに渡す前に、未使用の RTF 要素を文字列から削除することをお勧めします。

標準の RTF 文字エンコーディングメカニズムの代わりに、UTF-8 および ISO 標準に基づく言語エンコーディングが RTF 文字列でサポートされます。 これにより、アプリケーションは RTF エンコーディングの知識がなくても、英語以外のテキストをサーバーに送信できます。

文字列を http 経由で送信する場合は、HTTP に準拠していない文字はすべて適切にエスケープする必要があります。 文字列が画像カタログレコードの `catalog::Modifiers` フィールドに組み込まれている場合は、「=」、「&amp;」、「%」のみをエスケープする必要があります。 制御文字（`<CR>`、`<LF>`、`<TAB>` など）は常に削除する必要があります。

画像サービングテキストエンジンは、リッチテキスト形式（RTF）仕様バージョン 1.6 で定義されているコマンドのサブセットを解釈します。このサブセットは、フォント/文字の書式設定、単純な段落書式、国際フォントおよび文字セットのサポートに重点を置いています。 現時点では、スタイル シートやテーブルなど、より高度な書式構成はサポートされていません。

RTF エンコードされたテキスト文字列を手動で構築しようとする場合は、Microsoftで公開されているリッチテキスト形式（RTF）仕様に精通している必要があります。

* [フォントの処理](r-font-handling.md)
* [カラー処理](r-color-handling.md)
* [Copy-fitting](r-copy-fitting.md)
* [テキストレイヤー](r-text-layers.md)
* [テキストの配置](r-text-positioning.md)
* [予約文字](r-reserved-characters.md)
* [サポートされる RTF コマンドとキーワード](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF エンコーディングの例](r-rtf-encoding-examples.md)
