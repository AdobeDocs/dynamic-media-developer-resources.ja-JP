---
description: vntcは、stderrまたはログファイルに送信されるテキストデータを生成します。
seo-description: vntcは、stderrまたはログファイルに送信されるテキストデータを生成します。
seo-title: Output
solution: Experience Manager
title: Output
topic: Scene7 Image Serving - Image Rendering API
uuid: f2041600-408f-481c-95fc-3c112def7b8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '688'
ht-degree: 0%

---


# 出力{#output}

vntcは、stderrまたはログファイルに送信されるテキストデータを生成します。

データは、テキストレコードごとに1つの`name=value`プロパティとして形式設定されます。 文字列値は引用符で囲まれません。 `-log`が指定されている場合でも、警告メッセージとエラーメッセージは常に`stderr`に送信されます。

同じ出力で、特定のプロパティが複数回発生する場合があります。 0から始まるシーケンス番号がこれらのプロパティの名前に付加され、ピリオドで区切られます。 このようなプロパティは、次のようにプロパティ名の後に`. *`n`*`サフィックスが付きます。

次のプロパティが生成されます。

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>キャビネットスタイルのRGB背景色。 キャビネットスタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>デフォルトの出力ファイルのバージョンです。 また、このリリースの<span class="filepath"> vntc</span>で生成できる最も高いファイルバージョン番号です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">エラー.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>エラーメッセージ。 通常、エラーメッセージが表示される場合は、出力ファイルが作成されていないか、画像レンダリングでの使用に適していないことを示します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">ファイル.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>ビネット、キャビネットスタイルファイル、最大解像度画像、サムネール画像を含む、すべての出力ファイルの完全なパス/名前です。 生成される各ファイル（ログファイルを除く）に対して、1つのfile属性が存在します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> キャビネットにガラスのドアが含まれる場合は</span> ivalis 1、それ以外の場合は0。キャビネットスタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>に埋め込まれているiccProfileの名前。 </p> <p><span class="varname"> sourceFile</span>がカラーマネージメントでない場合は空です。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>進行状況などの情報メッセージ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> sourceFileがマスタービネットの場合は1、vnUpdateまたはvntcで以前に処理された場合は0 <span class="varname"> </span> を返し <span class="filepath"> </span>  <span class="filepath"> </span>ます。ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFileがJPEG画像データを含むキャビネットスタイルの場合は0</span> を、それ以外の場合は1を <span class="varname"> </span> 指定します。キャビネットおよび窓カバリングスタイルファイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>実行中の<span class="filepath"> vntc</span>プロセスに適用される最大メモリ制限です。 <span class="varname"> stringival</span> ,  <span class="varname"> ivalK</span>, ivalM <span class="varname"> M</span>, ival  <span class="varname"> val</span>, ival mM <span class="varname"> , ival val, g gg, 00 </span> <span class="codeph"> </span> disabled (disabled)のいずれかです。<span class="varname"> K</span>、<span class="varname"> M</span>、<span class="varname"> G</span>は、キロバイト（1024バイト）、メガバイト（1048576バイト）、およびギガバイト（1073741824バイト）を表します。. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネットの最も低い解像度のピラミッドレベルのスケール。 <span class="codeph"> -pyramid</span>が指定されている場合にのみ存在します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>に保存されたマテリアルの数。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>このキャビネットスタイルファイル内のパネル画像の数。 キャビネットスタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネットのピラミッドレベルの数。 -pyramidを指定した場合のみ存在します。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramid=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0は、コピー元ビネットまたはコピー先ビネットにピラミッド構造がある場合です。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>キャビネットスタイルの場合、<span class="varname"> sourceFile</span>のオブジェクト解像度。 ビネットの場合、これは、出力ビネットをレンダリングする際に、最高の画質でレンダリングされる結果を得るために推奨されるマテリアル解像度です。 ピクセル/インチ(ppi) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネット内のオブジェクト解像度の最小値です。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネットの平均オブジェクト解像度。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>完全修飾<span class="varname"> sourceFile</span>パス。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>のファイルバージョン。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>入力ビネットのピクセルサイズ、キャビネットスタイルファイル内の初期設定のパネル画像、または窓カバリングスタイルファイルの最初の不透明度画像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>ウィンドウカバリングのタイプ（ウィンドウカバリングのスタイルのみ）: </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0 =水平のシェードまたはブラインド </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=垂直ブラインド </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=全角短いカーテン </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=左/右のショートドレープ </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=全幅の全長カーテン </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=左/右フルレングスドレープ </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=カフェカーテン </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFileはビネット、 <span class="codeph"> </span> vncif  <span class="varname"> </span> sourceFileはキャビネットスタイル、または <span class="codeph"> </span> vnwif  <span class="varname"> </span> sourceFileは窓カバリングスタイルです。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> -version</span>で指定した値、または<span class="codeph"> -version</span>が指定されていない場合は<span class="codeph"> defaultFileVersion</span>の値。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span> nol]</span> </p></td> 
  <td class="stentry"> <p>出力ビネット(ビネットの最大リスト)、キャビネットスタイルファイル内の初期設定のパネル画像、またはウィンドウカバリングスタイルファイルの最初の表示画像のピクセルサイズのカンマ区切り表示。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> キャビネットスタイルがテクスチャ可能な場合は1、それ以外の場合は0を</span> 返します。ビネットおよびウィンドウカバリングのスタイルファイルには存在しません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">警告.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>警告メッセージ（<span class="codeph"> -imagemap</span>が指定されているが、ビネットにマップデータが見つからない場合など） </p></td> 
 </tr> 
</table>

