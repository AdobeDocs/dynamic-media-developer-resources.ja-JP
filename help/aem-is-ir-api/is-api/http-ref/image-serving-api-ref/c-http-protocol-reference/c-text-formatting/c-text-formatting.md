---
description: 画像サービングには、テキストをレンダリングするための複数の選択肢があり、text= コマンドとtextPs= コマンドを使用してアクセスできます。
solution: Experience Manager
title: テキスト書式設定
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2c120ed1-b556-4caf-a30e-63ae48cc2104
TQID: 'https://experienceleague.adobe.com/OzCs0opEKfoih79LE4UuXEOJnN4Zh6iBtQNdRxCddAE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 579
ht-degree: 6%

---

# テキスト書式設定{#text-formatting}

画像サービングには、テキストをレンダリングするための複数の選択肢があり、text= コマンドとtextPs= コマンドを使用してアクセスできます。

`textPs=`は、Adobe PhotoshopおよびIllustratorでレンダリングされたテキストと高レベルの類似性を提供します。 `text=`は、Windows Wordpadでレンダリングされたテキストと合理的に互換性があります。

>[!NOTE]
>
>他の場所に記載されている違いに加えて、`text=`は、`textPs=`と比較すると、レンダリングされたテキストの微妙な違いを生み出します。 例えば、下線の太さと位置は同じではなく、合成された斜体は少し異なる角度でレンダリングされます。 テキストが使用可能なスペースに収まらない場合、`text=`は最後の行を部分的に切り抜くことができ、`textPs=`は完全な行のみをレンダリングします。

すべてのテキストコマンドは、RTF （リッチテキスト形式）仕様のサブセットに基づく書式付きテキストを受け付けます。 各テキストレイヤーは、異なるテキストコマンドを指定できます。

次の表に、各テキストコマンドで使用できる主な機能を示します。

<table id="table_9C41CBDA94C24805B538E5049B0137C6"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>機能</b> </th> 
   <th class="entry"> <b> text=</b> </th> 
   <th class="entry"> <b> textPs=</b> </th> 
   <th class="entry"> <b>関連項目</b> </th> 
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
   <td> <p>テキストを任意のシェイプにフロー </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>textFlowPath=, textFlowXPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>任意のパスに沿ってテキストを流し込む </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>textPath= </p> </td> 
  </tr> 
  <tr> 
   <td> <p>コピーフィット </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> コピーフィット <p>, <pre>\copyfit</pre>, <pre>\copyfitlines</pre>, <pre>\copyfitmaxlines</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>テキストボックスの余白 </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><pre>\margl</pre>, <pre>\margr</pre>, <pre>\margt</pre>, <pre>\margb</pre> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>段落全体のジャスティフィケーション </p> </td> 
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
   <td> <p>すべての大文字と小文字 </p> </td> 
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
   <td> <p>上下/右左のテキストフロー </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>\stextFlow </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Photofont® サポート </p> </td> 
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
   <td> <p>レイヤーに合わせてテキストを自動的に拡大・縮小（解像度を変える） </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p>textAttr= </p> </td> 
  </tr> 
 </tbody> 
</table>

RTF準拠の文字列は、手動で組み立てるか、RTF ファイルを保存できるテキストエディターまたはワードプロセッサーで目的のテキストをフォーマットすることで組み立てることができます。 その後、RTF ファイルをプレーンテキストエディターで開き、リクエスト URLにコピーされたファイルの関連する生のRTF コンテンツを開くことができます。

一部のワードプロセッサーでは、かなり大きなファイルが生成されますが、これにはDynamic Media Image Servingでは使用されない大きなプリアンブルが含まれます。 未使用のRTF要素を文字列から削除してから、文字列をテキストコマンドに渡すことをお勧めします。

UTF-8およびISO規格に基づく言語エンコーディングは、標準のRTF文字エンコーディングメカニズムの代替として、RTF文字列でサポートされています。 これにより、アプリケーションはRTF エンコーディングの知識がなくても、英語以外のテキストをサーバーに送信できます。

文字列がhttpを介して送信される場合、HTTPに準拠していない文字はすべて適切にエスケープする必要があります。 文字列が画像カタログレコードの`catalog::Modifiers` フィールドに組み込まれている場合は、「=」、「&amp;」、「%」のみをエスケープする必要があります。 `<CR>`、`<LF>`、`<TAB>`などの制御文字は常に削除する必要があります。

画像サービングテキストエンジンは、リッチテキスト形式（RTF）仕様（バージョン 1.6）で定義されたコマンドのサブセットを解釈します。 このサブセットは、フォント/文字の書式設定、シンプルな段落の書式設定、国際的なフォントと文字セットのサポートに重点を置いています。 現在、スタイルシートや表など、より高度な書式設定はサポートされていません。

Microsoftによって公開されているリッチテキストフォーマット（RTF）仕様に精通している必要があるのは、RTF エンコードされたテキスト文字列を手動で作成しようとする場合です。

* [フォント処理](r-font-handling.md)
* [カラー処理](r-color-handling.md)
* [コピーフィット](r-copy-fitting.md)
* [テキストレイヤー](r-text-layers.md)
* [テキストの配置](r-text-positioning.md)
* [予約済み文字](r-reserved-characters.md)
* [サポートされているRTF コマンドとキーワード](c-supported-rtf-commands-and-keywords/c-supported-rtf-commands-and-keywords.md)
* [RTF エンコーディングの例](r-rtf-encoding-examples.md)
