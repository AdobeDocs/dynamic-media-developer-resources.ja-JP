---
description: vntcは、stderrまたはログファイルに送信されるテキストデータを生成します。
solution: Experience Manager
title: 出力
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# 出力{#output}

vntcは、stderrまたはログファイルに送信されるテキストデータを生成します。

データは、テキストレコードごとに1つの`name=value`プロパティとして形式設定されます。 文字列値は引用符で囲まれません。 `-log`が指定されている場合でも、警告メッセージとエラーメッセージは常に`stderr`に送信されます。

同じ出力で特定のプロパティが複数回発生する場合があります。 0から始まるシーケンス番号が、これらのプロパティの名前にピリオドで区切って追加されます。 このようなプロパティは、以下でプロパティ名の後に`. *`n`*`サフィックスが付きます。

次のプロパティが生成されます。

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>, <span class="varname"> ival</span>, <span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>キャビネットスタイルのRGB背景色。 キャビネットスタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>デフォルトの出力ファイルのバージョン。 また、このリリースの<span class="filepath"> vntc</span>で生成できる最も高いファイルバージョン番号です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">エラー.<span class="varname"> n</span>=<span class="varname"> 文字列</span></span> </p></td> 
  <td class="stentry"> <p>エラーメッセージ。 エラーメッセージが表示されるのは、通常、出力ファイルが作成されていないか、画像レンダリングでの使用に適していないことを示します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">ファイル.<span class="varname"> n</span>=<span class="varname"> 文字列</span></span> </p></td> 
  <td class="stentry"> <p>ビネット、キャビネットスタイルファイル、最大解像度画像、サムネール画像を含む、すべての出力ファイルの完全修飾パス/名前。 生成されたファイル（ログファイルを除く）ごとに1つのファイル属性が存在します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> キャビネットにガラスのドアが含まれる場合は1、それ以外の場合は0を指定します。キャビネットスタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>に埋め込まれたiccProfileの名前。 </p> <p><span class="varname"> sourceFile</span>がカラーマネージメントでない場合は空です。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> 文字列</span></span> </p></td> 
  <td class="stentry"> <p>進行状況情報などの情報メッセージ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> ivalis 1はsourceFileがマ <span class="varname"> </span> スタービネットの場合、0はvnUpdateまたはvntcで以前に処理さ <span class="filepath"> </span> れた場 <span class="filepath"> 合です</span>。ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> sourceFileがJPEG画像デ <span class="varname"> </span> ータを含むキャビネットスタイルの場合は0（この場合は警告も出力されます）、それ以外の場合は1になります。キャビネットと窓カバースタイルファイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>実行中の<span class="filepath"> vntc</span>プロセスに適用される最大メモリ制限。 <span class="varname"> </span> stringは、 <span class="varname"> ival</span>、 <span class="varname"> ivalK</span>、 <span class="varname"> ivalM</span>、 <span class="varname"> ivalG</span>、または <span class="codeph"> 0</span> （無効）のいずれかです。<span class="varname"> K</span>、<span class="varname"> M</span>、<span class="varname"> G</span>は、キロバイト（1024バイト）、メガバイト(1048576バイト)、ギガバイト(1073741824バイト)を表します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネットの最も低い解像度のピラミッドレベルのスケール。 <span class="codeph"> -pyramid</span>を指定した場合にのみ存在します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>に保存されたマテリアルの数。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>このキャビネットスタイルファイル内のパネルイメージの数。 キャビネットスタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネットのピラミッドレベルの数。 -pyramidを指定した場合のみ存在します。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramid=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>ソースビネットまたは宛先ビネットにピラミッド構造がある場合は0 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>キャビネットスタイルの場合、<span class="varname"> sourceFile</span>のオブジェクト解像度。 ビネットの場合は、出力ビネットをレンダリングする際に最高品質のレンダリング結果を得るために推奨されるマテリアル解像度です。 ピクセル/インチ(ppi) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネットの最小のオブジェクト解像度。 ビネットのみ。 </p></td> 
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
  <td class="stentry"> <p>入力ビネットのピクセルサイズ、キャビネットスタイルファイル内のデフォルトのパネル画像、またはウィンドウカバースタイルファイルの最初の不透明度画像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>窓の覆いのタイプ（窓の覆いのスタイルのみ）: </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0 =水平のシェードまたはブラインド </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=垂直ブラインド </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=全角短いカーテン </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=左/右ショートドレープ </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=全幅のカーテン </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=左/右フルレングスドレープ </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=café curtain </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> </span> vntif  <span class="varname"> </span> sourceFileはビネット、 vncif  <span class="codeph"> </span> sourceFileはキャビネッ <span class="varname"> </span> トスタイル、またはvnwif  <span class="codeph"> </span>  <span class="varname"> </span> sourceFileは窓カバースタイルです。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> -version</span>で指定された値、または<span class="codeph"> defaultFileVersion</span>の値（<span class="codeph"> -version</span>が指定されていない場合）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>, <span class="varname"> ival</span> *[, <span class="varname"> ival</span>, <span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>出力ビネット（ピラミッドビネットの最大解像度ビュー）、キャビネットスタイルファイルの既定のパネル画像、またはウィンドウカバースタイルファイルの最初の不透明度画像のピクセルサイズのコンマ区切りリスト。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> </span> キャビネットスタイルがテクスチャ可能な場合は1、それ以外の場合は0を返します。ビネットとウィンドウカバーのスタイルファイルには存在しません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">警告.<span class="varname"> n</span>=<span class="varname"> 文字列</span></span> </p></td> 
  <td class="stentry"> <p>警告メッセージ（<span class="codeph"> -imagemap</span>が指定されていて、ビネットにマップデータが見つからない場合など）。 </p></td> 
 </tr> 
</table>
