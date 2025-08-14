---
description: vntc は、テキスト・データを生成し、stderr またはログ・ファイルに送信します。
solution: Experience Manager
title: 出力
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# 出力{#output}

vntc は、テキスト・データを生成し、stderr またはログ・ファイルに送信します。

データは、テキストレコードごとに 1 つの `name=value` プロパティとしてフォーマットされます。 文字列値は引用符で囲まれていません。 `stderr` が指定されている場合でも、警告およびエラーメッセージは常に `-log` に送信されます。

特定のプロパティは、同じ出力で複数回発生する可能性があります。 0 から始まるシーケンス番号が、これらのプロパティの名前にピリオドで区切って追加されます。 このようなプロパティは、プロパティ名の後に `. *`n`*` サフィックスを付けて以下に示します。

次のプロパティが生成されます。

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>キャビネットスタイルのRGBの背景色 キャビネット スタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>デフォルトの出力ファイルのバージョン。 また、このリリースの vntc<span class="filepath"> で生成できる最も高いファイル バージョン番号 </span> あります。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> エラー。<span class="varname"> n</span>=<span class="varname"> 文字列 </span></span> </p></td> 
  <td class="stentry"> <p>エラーメッセージ。 エラーメッセージが表示される場合は、通常、出力ファイルが作成されていないか、画像レンダリングでの使用に適していないことを示します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> ファイル。<span class="varname"> n</span>=<span class="varname"> 文字列 </span></span> </p></td> 
  <td class="stentry"> <p>ビネット、キャビネット スタイル ファイル、フル解像度の画像、サムネイル画像を含む、すべての出力ファイルの完全修飾パス/名前。 生成されたファイル（ログファイルを除く）ごとに 1 つのファイル属性が存在します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>キャビネットにガラス ドアが含まれる場合は <span class="varname"> ival</span> は 1、それ以外の場合は 0 です。 キャビネット スタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span> に埋め込まれた iccProfile の名前。 </p> <p>sourceFile<span class="varname"> がカラ </span> 管理されていない場合は空です。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 情報。<span class="varname"> n</span>=<span class="varname"> 文字列 </span></span> </p></td> 
  <td class="stentry"> <p>情報メッセージ（進行状況情報など）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span> がマスターのビネットの場合 <span class="varname">ival</span> は 1、vnUpdate<span class="filepath"> または vntc</span> で以前に処理されてい <span class="filepath"> 場合 </span>0 です。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>sourceFile<span class="varname"> がJPEG画像データを含むキャビネットスタイルの場合 </span>ival<span class="varname"> が 0 である </span> （この場合は警告も出力されます）、それ以外の場合は 1 です。 スタイル ファイルのみをカバーするキャビネットと窓。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>実行中の <span class="filepath"> vntc</span> プロセスに適用される最大メモリ制限です。 文字列 <span class="varname"></span>、<span class="varname"> ival</span>、<span class="varname"> ivalK</span>、<span class="varname"> ivalM</span>、<span class="varname"> ivalG</span>、<span class="codeph"> 0</span> （無効）のいずれかです。 ここで、<span class="varname"> K</span>、<span class="varname"> M</span> および <span class="varname"> G</span> は、キロバイト（1024 バイト）、メガバイト（1048576 バイト）、ギガバイト（1073741824 バイト）を表します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネットの最も低い解像度のピラミッドレベルのスケール。 -pyramid<span class="codeph"> が指定され </span> いる場合にのみ存在します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span> に保存されたマテリアルの数。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>このキャビネットスタイルファイル内のパネルイメージの数。 キャビネット スタイルのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネット内のピラミッドレベルの数。 -pyramid が指定されている場合にのみ存在します。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> ピラミッド=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>ソースまたは宛先のビネットがピラミッド構造を持つ場合は 0。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>キャビネットスタイルの場合、<span class="varname"> sourceFile</span> のオブジェクト解像度。 ビネットの場合、これは出力ビネットをレンダリングする際に最適な品質のレンダリング結果を得るための推奨マテリアル解像度です。 ピクセル/インチ（ppi） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネットの最小オブジェクト解像度。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>出力ビネット内のオブジェクトの平均解像度。 ビネットのみ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span> の完全修飾パス。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>sourceFile<span class="varname"> のファイル </span> バージョン。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>入力ビネットのピクセルサイズ、キャビネットスタイルファイル内のデフォルトのパネルイメージ、またはスタイルファイルをカバーするウィンドウの最初の不透明度イメージ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>ウィンドウの覆いのタイプ（ウィンドウの覆いのスタイルのみ）: </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=水平シェードまたはブラインド </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=垂直ブラインド </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=全幅の短いカーテン </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=左右の短いドレープ </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=全幅フルレングスのカーテン </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=左/右の全長ドレープ </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=カフェカーテン </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=ヴァランス </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>vnt<span class="codeph"></span> sourceFile<span class="varname"> がビネットの場合 </span>vnc<span class="codeph">sourceFile</span> がキャビネットスタイルの場合 <span class="varname">vnc</span>、sourceFile<span class="codeph"> がウィンドウカバースタイルの場合 </span>vnw<span class="varname"> を </span> します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> -version</span> で指定された値、または <span class="codeph"> defaultFileVersion</span> if<span class="codeph"> -version</span> の値が指定されていませんでした。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>,<span class="varname"> ival</span>*[,<span class="varname"> ival</span>,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>出力ビネット（ピラミッド型ビネットのフル解像度表示）内のすべてのビュー、キャビネットスタイルファイル内のデフォルトパネルイメージ、またはスタイルファイルを覆うウィンドウの最初の不透明度イメージのピクセルサイズのコンマ区切りリスト。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>キャビネット スタイルがテキス <span class="varname"> 可能な場合は ival</span> は 1、それ以外の場合は 0 です。 ビネットおよびウィンドウのカバーリング スタイル ファイルには存在しません。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 警告。<span class="varname"> n</span>=<span class="varname"> 文字列 </span></span> </p></td> 
  <td class="stentry"> <p>警告メッセージ（– imagemap<span class="codeph"> 指定されているが </span> ビネット内にマップデータが見つからない場合など）。 </p></td> 
 </tr> 
</table>
