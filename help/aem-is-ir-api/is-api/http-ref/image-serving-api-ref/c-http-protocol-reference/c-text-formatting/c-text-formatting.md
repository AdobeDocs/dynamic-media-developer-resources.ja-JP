---
description: 画像サービングには、テキストをレンダリングするいくつかの代替方法が用意されており、text=およびtextPs=コマンドを使用してアクセスできます。
seo-description: 画像サービングには、テキストをレンダリングするいくつかの代替方法が用意されており、text=およびtextPs=コマンドを使用してアクセスできます。
seo-title: テキストの書式設定
solution: Experience Manager
title: テキストの書式設定
topic: Scene7 Image Serving - Image Rendering API
uuid: e67b6dd2-2a78-4014-9525-816d91c9e783
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# テキストの書式設定{#text-formatting}

画像サービングには、テキストをレンダリングするいくつかの代替方法が用意されており、text=およびtextPs=コマンドを使用してアクセスできます。

`textPs=` は、Adobe PhotoshopおよびIllustratorでレンダリングされたテキストとの類似性の高いレベルを提供します。 `text=` は、Windows Wordpadでレンダリングされたテキストと適切に互換性があります。

>[!NOTE]
>
>他の場所に示した違いに加えて、と比較して、レ `text=` ンダリングされたテキストに微妙な違いが生じます `textPs=`。 例えば、下線の太さと位置が同じではなく、合成された斜体が少し異なる角度でレンダリングされます。 テキストが使用可能なスペースに収まらない場合は、最 `text=` 後の行が部分的に切り抜かれ、一方で行全体がレ `textPs=` ンダリングされることがあります。

すべてのテキストコマンドは、RTF（リッチテキスト形式）仕様のサブセットに基づいて、形式設定されたテキストを受け付けます。 各テキストレイヤーには、異なるテキストコマンドを指定できます。

次の表に、各テキストリストで使用できる主な機能を示します。

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
   <td> <p>テキストを任意の図形に流し込む </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>textFlowPath=、textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>任意のパスに沿ってテキストをフロー </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>コピー継手 </p> </td> 
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
   <td> <p>段落全体の行揃え </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><pre>\qj</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>最終行の位置揃え </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\lastql, \lastqr, \lastqc, \lastqj </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落のインデント </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\fi、\li、\ri </p> </td> 
  </tr> 
  <tr> 
   <td> <p>オールキャップスとスモールキャップスのテキスト </p> </td> 
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
   <td> <p>上下右のテキストフロー </p> </td> 
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
   <td> <p>テキストに合わせてレイヤーのサイズを自動調整 </p> </td> 
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
   <td> <p>右から左への文字フロー </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>\rtlch </p> </td> 
  </tr> 
  <tr> 
   <td> <p>折り返しの無効化 </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>レイヤーに合わせてテキストを自動スケール（解像度を変更） </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF準拠の文字列は、手動でアセンブルするか、RTFファイルを保存できるテキストエディタまたはワードプロセッサで必要なテキストをフォーマットしてアセンブリできます。 その後、RTFファイルをプレーンテキストエディタで開き、そのファイルの関連する生のRTFコンテンツを要求URLにコピーできます。

一部のワードプロセッサーでは、Scene7画像サービングで使用されない大きなプリアンブルを含む、かなり大きなファイルが生成されます。 文字列をテキストコマンドに渡す前に、未使用のRTF要素を文字列から削除することをお勧めします。

UTF-8およびISO規格に基づく言語エンコーディングは、標準のRTF文字エンコーディングメカニズムに代わるRTF文字列でサポートされています。 これにより、アプリケーションは英語以外のテキストをRTFエンコーディングの知識なしでサーバに送信できます。

文字列をhttp経由で送信する場合は、HTTPに準拠していないすべての文字を適切にエスケープする必要があります。 文字列を画像カタログレコードのフィールドに組み込む場合は、「=」、「&amp;」および「%」のみエスケ `catalog::Modifiers` ープする必要があります。 、およびを含む制御文 `<CR>`字は、 `<LF>`常に削 `<TAB>` 除する必要があります。

画像サービングテキストエンジンは、リッチテキスト形式(RTF)仕様のバージョン1.6で定義されたコマンドのサブセットを解釈します。このサブセットは、フォント/文字の書式設定、単純な段落の書式設定、および国際フォントと文字セットのサポートに重点を置いています。 現時点では、スタイルシートやテーブルなど、より高度な書式設定構成はサポートされていません。

RTFエンコードされたテキスト文字列を手動で作成する場合は、Microsoftが発行したRich Text Format(RTF)仕様に精通している必要があります。

* [フォント処理](r-font-handling.md)
* [カラー処理](r-color-handling.md)
* [コピー継手](r-copy-fitting.md)
* [テキストレイヤー](r-text-layers.md)
* [テキストの位置](r-text-positioning.md)
* [予約文字](r-reserved-characters.md)
* [サポートされるRTFコマンドとキーワード](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTFエンコーディングの例](r-rtf-encoding-examples.md)
