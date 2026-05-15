---
description: vntcは、stderrまたはログファイルに送信されるテキストデータを生成します。
solution: Experience Manager
title: Output
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
TQID: 'https://experienceleague.adobe.com/XYdTYt0N200rDYSl4klx7c0kfsDY-650TOy9-ui4cvw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 702
ht-degree: 0%

---

# Output{#output}

vntcは、stderrまたはログファイルに送信されるテキストデータを生成します。

データは、テキストレコードごとに1つの`name=value` プロパティとして書式設定されます。 文字列値は引用符で囲まれていません。 `-log`が指定されている場合でも、警告メッセージとエラーメッセージは常に`stderr`に送信されます。

特定のプロパティは、同じ出力で複数回発生する可能性があります。 これらのプロパティの名前には、0から始まるシーケンス番号がピリオドで区切って追加されます。 このようなプロパティは、プロパティ名の後に`. *`n`*`接尾辞を付けて以下に示します。

次のプロパティが生成されます。

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>キャビネットスタイルのRGB背景色。 キャビネット スタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>デフォルトの出力ファイルバージョン。 また、このリリースの<span class="filepath"> vntc</span>が生成できる最高のファイルバージョン番号です。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> エラー。<span class="varname"> n</span>=<span class="varname">文字列</span></span> </p></td> 
  <td class="stentry"> <p>エラーメッセージ。 エラーメッセージが表示される場合は、通常、出力ファイルが作成されていないか、画像レンダリングでの使用に適していないことを示します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> ファイル。<span class="varname"> n</span>=<span class="varname">文字列</span></span> </p></td> 
  <td class="stentry"> <p>ビネット、キャビネットのスタイルファイル、完全解像度画像、サムネール画像など、すべての出力ファイルの完全修飾パスまたは名前。 生成された各ファイル（ログファイルを除く）に1つのファイル属性が存在します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>キャビネットにガラスのドアが含まれている場合は<span class="varname"> ival</span>は1で、それ以外の場合は0です。 キャビネット スタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname">文字列</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>に埋め込まれたiccProfileの名前。 </p> <p><span class="varname"> sourceFile</span>がカラーマネジメントされていない場合は空です。 周辺光量補正のみ </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">情報。<span class="varname"> n</span>=<span class="varname">文字列</span></span> </p></td> 
  <td class="stentry"> <p>情報メッセージ：進捗情報など </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span>は、<span class="varname"> sourceFile</span>がマスタービネットである場合は1で、<span class="filepath"> vnUpdate</span>または<span class="filepath"> vntc</span>で以前に処理された場合は0です。 周辺光量補正のみ </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> ival</span>が0です。<span class="varname"> sourceFile</span>がJPEG画像データを含むキャビネットスタイルである場合（この場合は警告も出力されます）、それ以外の場合は1です。 キャビネットとウィンドウはスタイルファイルのみをカバーします。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname">文字列</span></span> </p></td> 
  <td class="stentry"> <p>実行中の<span class="filepath"> vntc</span> プロセスに適用される最大メモリ制限です。 <span class="varname">文字列</span>は、<span class="varname"> ival</span>、<span class="varname"> ivalK</span>、<span class="varname"> ivalM</span>、<span class="varname"> ivalG</span>または<span class="codeph"> 0</span>のいずれかです（無効）。 ここで、<span class="varname"> K</span>、<span class="varname"> M</span>、<span class="varname"> G</span>は、キロバイト（1024 バイト）、メガバイト（1048576 バイト）、およびギガバイト（1073741824 バイト）を表します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネット内の最も解像度の低いピラミッド レベルのスケール。 <span class="codeph"> – ピラミッド </span>が指定されている場合にのみ存在します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>に保存されたマテリアルの数。 周辺光量補正のみ </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>このキャビネットスタイルファイル内のパネル画像の数。 キャビネット スタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネット内のピラミッドレベルの数。 -pyramidが指定されている場合にのみ存在します。 周辺光量補正のみ </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> ピラミッド=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>ソースまたは宛先のビネットにピラミッド構造がある場合は0です。 周辺光量補正のみ </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>キャビネット スタイルの場合、<span class="varname"> sourceFile</span>のオブジェクト解決。 周辺光量補正の場合、出力ビネットをレンダリングする際に、最高品質のレンダリング結果を得るために推奨されるマテリアル解像度です。 ピクセル/インチ（ppi）: </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネット内の最小オブジェクト解像度。 周辺光量補正のみ </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネット内のオブジェクトの平均解像度。 周辺光量補正のみ </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname">文字列</span></span> </p></td> 
  <td class="stentry"> <p>完全修飾<span class="varname"> sourceFile</span> パス。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>のファイル バージョン。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>入力ビネットのピクセルサイズ、キャビネットスタイルファイル内のデフォルトのパネル画像、またはウィンドウカバースタイルファイルの最初の不透明度画像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname">文字列</span></span> </p></td> 
  <td class="stentry"> <p>窓カバーの種類（窓カバーのスタイルのみ）: </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=水平シェードまたはブラインド </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=垂直ブラインド </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=全幅の短いカーテン </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=左/右の短いドレープ </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=全幅フルレングスカーテン </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=左/右フルレングスドレープ </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=カフェカーテン </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=バランス </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname">文字列</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> （<span class="varname"> sourceFile</span>がビネットの場合）、<span class="codeph"> vnc</span> （<span class="varname"> sourceFile</span>がキャビネットスタイルの場合）、<span class="codeph"> vnw</span> （<span class="varname"> sourceFile</span>がウィンドウのカバーのスタイルの場合）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> -version</span>で指定された値、または<span class="codeph"> -version</span>が指定されていない場合の<span class="codeph"> defaultFileVersion</span>の値。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>出力ビネット内のすべてのビュー（ピラミッドのビネットの全解像度ビュー）、キャビネットスタイルファイル内のデフォルトのパネル画像、またはスタイルファイルをカバーするウィンドウの最初の不透明度画像のピクセルサイズをコンマ区切りで示します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>キャビネット スタイルがテクスチャ可能な場合は<span class="varname"> ival</span>が1で、それ以外の場合は0です。 ビネットとウィンドウのカバリングスタイルファイルには存在しません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">警告。<span class="varname"> n</span>=<span class="varname">文字列</span></span> </p></td> 
  <td class="stentry"> <p>警告メッセージ（<span class="codeph"> -imagemap</span>が指定されていても、周辺光量補正にマップデータが見つからない場合など）。 </p></td> 
 </tr> 
</table>
