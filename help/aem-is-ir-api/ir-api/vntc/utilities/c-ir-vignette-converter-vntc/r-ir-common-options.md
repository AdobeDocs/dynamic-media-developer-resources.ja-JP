---
title: 共通オプション
description: sourceFileのタイプに関係なく、次のオプションを適用できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
TQID: 'https://experienceleague.adobe.com/3Wz0goEJBDZmEomYaszS1Am7GMuTBxWEl1l-6Y163J0'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 704
ht-degree: 0%

---

# 共通オプション{#common-options}

sourceFileのタイプに関係なく、次のオプションを適用できます。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname">文字列</span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルを配置するフォルダー（<span class="codeph"> -log </span>が指定されている場合はログファイルを含む）。 絶対パスまたは現在の作業ディレクトリへの相対パスを指定できます。 フォルダー階層は存在しない場合に作成されますが、<span class="codeph"> -log </span>で指定されたファイルには適用されません。 指定しない場合、出力ファイルは、<span class="varname"> sourceFile </span>が格納されているフォルダーに書き込まれます。 <span class="varname"> destFile </span>が指定されている場合、常にその場所に書き込まれ、<span class="codeph"> -destpath </span>はセカンダリ出力ファイルにのみ適用されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> – 画像</span> </p> </td> 
  <td class="stentry"> <p>指定された場合、（最初の）ビュー画像は、周辺光量補正、キャビネットスタイルからの適切なパネル画像、またはウィンドウ覆いスタイルの最初の照明画像から抽出されます。 抽出した画像は、フル解像度のTIFF ファイルとして保存されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>ターゲットファイルの生成を防止します。 <span class="varname"> ソースファイル </span>から属性をすばやく抽出するのに便利です。 オプションのサムネール （<span class="codeph"> -thumbwidth </span>）、画像（<span class="codeph"> -image </span>）、およびログファイル （<span class="codeph"> -log </span>）のみが生成されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルに埋め込まれたRGBとグレースケール画像データに対して、可逆PNGではなく、非可逆JPEG エンコーディングを選択します。 アルファ（RGBA）を含む画像は、常にPNG エンコーディングを使用して保存されます。 <span class="varname"> ival </span>は、JPEGの画質（1...100）を指定します。85以上をお勧めします。 デフォルトは<span class="codeph"> -jpegquality 0 </span>で、PNG エンコーディングを選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> – ログ <span class="varname"> パス </span> </span> </p> </td> 
  <td class="stentry"> <p>指定したパスまたは名前を持つログファイルを作成します。 宛先フォルダーに書き込まれたすべての出力ファイルのフルパスがログファイルに書き込まれ、バージョン情報や発生した警告やエラーなどの追加の設定が行われます（詳細は<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local">出力</a>を参照）。 <span class="codeph"> -log </span>が指定されていない場合、ログファイルは作成されません。この場合、すべてのテキスト出力は<span class="codeph"> stdout </span>に書き込まれます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> – 優先度が低い<span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="filepath"> vntc </span> プロセスの優先度を下げます。 このプロセスを使用すると、周辺光量補正の処理中に<span class="filepath"> vntc </span>がCPU全体を引き継ぐことがなくなります。 これにより、オペレーティングシステムは、他の、より重要な、プロセスにより多くの時間を与えることができます。 <span class="varname"> ival </span>は、優先度の低い割合（0..100）を指定します。 デフォルトは<span class="codeph"> -lowerpriority 0 </span>で、<span class="filepath"> vntc </span> プロセスの優先度を下げません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="filepath"> vntc </span>が使用できるメモリの最大量をバイト単位で指定します。 <span class="filepath"> vntc </span>がメモリの上限に達すると、処理を停止し、エラーが発生します。 <span class="varname"> ival </span>は、最大メモリ制限をバイト単位で指定します（0..3,758,096,384 （3.5 GB）。 <span class="varname"> ival </span>が0の場合、最大メモリ制限はオフになります。 デフォルトは<span class="codeph"> -maxmem 3221225472 </span>で、最大メモリ制限は3 GBです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> – 区切り記号" <span class="varname">文字列</span>" </span> </p> </td> 
  <td class="stentry"> <p>自動生成された出力ファイル名のファイル名とサイズ/解像度のサフィックスの間に配置される区切り文字を指定します。 指定しない場合、デフォルトは「 – 」になります。 <span class="varname"> destFile </span>または<span class="codeph"> -info </span>が指定されている場合、無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> – シャープ <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>処理中に画像をシャープ化（拡大・縮小）できます。 キャビネット形式のファイルのサムネールのシャープ化にのみ適用されます。 </p> <p>シャープを無効にする場合は0を指定します（デフォルト）。通常のシャープを有効にする場合は1を指定します。明るさのみのアンシャープマスクを有効にする場合は2を指定します。各カラーコンポーネントにアンシャープマスクを有効にする場合は3を指定します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>ログレベルを設定します。 デフォルトは1で、すべての情報、警告、エラーメッセージを出力します。 エラーメッセージ以外をすべて無効にするには、0に設定します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname">金額</span> <span class="varname">半径</span> <span class="varname">しきい値</span> </span> </p> </td> 
  <td class="stentry"> <p>アンシャープマスクのパラメーターを設定します。 <span class="codeph"> – シャープ </span>が0または1に設定されている場合は無視されます。<span class="codeph"> – シャープ </span>が2または3に設定されている場合は必須です。 <span class="varname">量</span>は0.0...500.0の範囲の実数値であり、<span class="varname">半径</span>は0.0...10.0の範囲の実数値であり、<span class="varname">しきい値</span>は0 ～ 255の整数です。 詳細については、「イメージ サービング プロトコル リファレンス」の<span class="codeph"> op_usm= </span>の説明を参照してください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>指定したビネットが適切な実稼動ビネットであることを検証します。 <span class="varname"> ival </span>は、ビネットの最小ファイル バージョンを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルのファイルバージョン。 指定する場合は、0または有効なビネットファイルバージョン（デフォルトのファイルバージョン以下）である必要があります。 0に設定するか、指定しない場合、出力ファイルは最新のファイルバージョンを使用して作成されます。 <span class="codeph"> -info </span>が指定されている場合は無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> – バージョン情報</span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 ファイル名やその他のオプションを指定せずに指定します。 </p> </td> 
 </tr> 
</table>
