---
description: vntcは、stderrまたはログファイルに送信されるテキストデータを生成します。
seo-description: vntcは、stderrまたはログファイルに送信されるテキストデータを生成します。
seo-title: 出力
solution: Experience Manager
title: 出力
topic: Scene7 Image Serving - Image Rendering API
uuid: f2041600-408f-481c-95fc-3c112def7b8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Output{#output}

vntcは、stderrまたはログファイルに送信されるテキストデータを生成します。

データは、テキストレコードごとに1つのプロ `name=value` パティとして形式設定されます。 文字列値は引用符で囲まれません。 警告メッセージとエラーメッセージは、指定されて `stderr`いる場合でも常に `-log` 送信されます。

同じ出力で、特定のプロパティが複数回発生する場合があります。 0から始まるシーケンス番号が、これらのプロパティの名前にピリオドで区切って追加されます。 このようなプロパティは、プロパティ名の後に `. *``*` nというサフィックスが付いています。

次のプロパティが生成されます。

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,ival<span class="varname"> ,ival</span><span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>キャビネットスタイルのRGB背景色。 キャビネットのスタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>デフォルトの出力ファイルのバージョン。 また、このリリースのvntcで生成できる最も高いファイルバ <span class="filepath"> ージョン</span> 番号です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">エラー.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>エラーメッセージ。 通常、エラーメッセージが表示される場合は、出力ファイルが作成されていないか、画像レンダリングでの使用に適していないことを示します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">ファイル.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>ビネット、キャビネットスタイルのファイル、最大解像度の画像、サムネール画像を含む、すべての出力ファイルの完全なパス/名前。 生成される各ファイル（ログファイルを除く）に対して1つのファイル属性が存在します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ivalは</span> 、キャビネットにガラスのドアが含まれる場合は1、それ以外の場合は0です。 キャビネットのスタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>sourceFileに埋め込まれたiccProfileの名 <span class="varname"> 前</span>。 </p> <p>sourceFileがカラーマ <span class="varname"> ネジメント</span> されていない場合は空です。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>進行状況などの情報メッセージ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFileがマスタビネッ</span> トの場合 <span class="varname"> 、ivalは1で、vnUpdateまたはvntcを使用して以前に処理された場合は</span> 0です <span class="filepath"></span><span class="filepath"></span>。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFileが</span> JPEG画像データを含むキャビネットスタイルの場合 <span class="varname"></span> 、ivalは0、それ以外の場合は1です。 キャビネットおよび窓カバリングスタイルファイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>実行中の <span class="filepath"> vntc</span> . <span class="varname"> string</span> は、ival <span class="varname"> 、ivalK、</span>ivalM <span class="varname"></span>、val <span class="varname"> G、0、0のいずれか</span><span class="varname"></span><span class="codeph"></span> です。 ここで、 <span class="varname"> K</span>、 <span class="varname"> M</span>、 <span class="varname"></span> Gは、キロバイト（1024バイト）、メガバイト（1048576バイト）、ギガバイト（1073741824バイト）を表します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネットの最も低い解像度のピラミッドレベルのスケール。 -pyramidが指定され <span class="codeph"> た場合</span> のみ存在します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>sourceFileに保存されたマテリアルの <span class="varname"> 数</span>。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>このキャビネットスタイルファイル内のパネルイメージの数。 キャビネットのスタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネットのピラミッドレベルの数。 -pyramidが指定された場合のみ存在します。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">pyramid=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>0（元のビネットまたは宛先のビネットがピラミッド構造の場合）。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>キャビネットスタイルの場合、sourceFileのオブジェクト解像度<span class="varname"> です</span>。 ビネットの場合、出力ビネットをレンダリングする際に、最高の画質でレンダリングするために推奨されるマテリアル解像度です。 ピクセル/インチ(ppi) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネット内のオブジェクトの最小解像度。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネットの平均オブジェクト解像度。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>完全修飾のsourceFile <span class="varname"> パス</span> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>sourceFileのファイルバージ <span class="varname"> ョン</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>入力ビネットのピクセルサイズ、キャビネットスタイルファイル内の初期設定のパネル画像、またはウィンドウカバリングスタイルファイルの最初の不透明度画像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>ウィンドウカバリングのタイプ（ウィンドウカバリングのスタイルのみ）: </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0 =水平のシェードまたはブラインド </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1 =垂直ブラインド </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=全角短いカーテン </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=左右の短いドレープ </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=全角のカーテン </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=左/右最大長ドレープ </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=カフェカーテン </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> sourceFileはビネット、vnc <span class="varname"> (sourceFile)はキャビネットスタイル、vnw(</span> source)はキャビネットスタイル、vnw( <span class="codeph"></span><span class="varname"></span><span class="codeph"></span><span class="varname"></span> source)はウィンドウスタイルです。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>-versionで指定された値 <span class="codeph"> 。-version</span>が指定されていない場合は<span class="codeph"> 、defaultFileVersionの値</span><span class="codeph"></span> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes<span class="varname"> ,</span>ival<span class="varname"> *[, ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span>not]</span> </p></td> 
  <td class="stentry"> <p>出力ビネット（ピラミッドビネットの最大解像度ビュー）、キャビネットスタイルファイル内の既定のパネル画像、またはウィンドウカバリングスタイルファイルの最初の不透明度画像のピクセルサイズのコンマ区切りリスト。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> キャビネットのスタイルがテクスチャ可能な場合は</span> 、ivalは1、それ以外の場合は0です。 ビネットおよびウィンドウカバリングのスタイルファイルには存在しません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">警告.<span class="varname"> n</span>=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>警告メッセージ( <span class="codeph"> -imagemapが指定されているが</span> 、ビネットにマップデータが見つからない場合など)。 </p></td> 
 </tr> 
</table>

