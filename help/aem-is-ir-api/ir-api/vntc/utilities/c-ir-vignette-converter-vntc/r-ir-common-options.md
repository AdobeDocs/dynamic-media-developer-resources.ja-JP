---
description: sourceFileの種類に関係なく、次のオプションを適用できます。
seo-description: sourceFileの種類に関係なく、次のオプションを適用できます。
seo-title: 一般的なオプション
solution: Experience Manager
title: 一般的なオプション
topic: Scene7 Image Serving - Image Rendering API
uuid: fdf09873-4102-4ed6-a315-a87cba5c44c7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 一般的なオプション{#common-options}

sourceFileの種類に関係なく、次のオプションを適用できます。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath文 <span class="varname"> 字 </span> 列 </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルを配置するフォルダー(-logを指定した場合は、ログフ <span class="codeph"> ァイルを </span> 含む)。 は、絶対パスまたは現在の作業ディレクトリからの相対パスです。 フォルダ階層が存在しない場合は作成されます。 -logで指定されたファイルには適用さ <span class="codeph"> れませ </span>ん。 指定しなかった場合、出力ファイルはsourceFileが存在するフォルダーに <span class="varname"> 書き込 </span> まれます。 destFileを指 <span class="varname"> 定し </span> た場合、そのファイルは常にその場所に書き込まれ、 <span class="codeph"> -destpathはセカ </span> ンダリ出力ファイルにのみ適用されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -イメージ </span> </p> </td> 
  <td class="stentry"> <p>指定した場合、（最初の）ビュー画像はビネット、キャビネットスタイルの適切なパネル画像、または窓カバリングスタイルの最初の照明画像から抽出されます。 抽出した画像は、最大解像度のTIFFファイルとして保存されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>ターゲットファイルの生成を防ぎます。 sourceFileからアトリビュートをすばやく抽出する <span class="varname"> 場合に役立 </span>ちます。 オプションのサムネール( <span class="codeph"> -thumbwidth </span>)、画像( <span class="codeph"> -image </span>)、ログファイル( <span class="codeph"> -log </span>)のみが生成されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>出力ファイルに埋め込まれたRGBおよびグレースケールの画像データに、可逆圧縮PNGではなく非可逆圧縮JPEGエンコーディングを選択します。 アルファ(RGBA)を持つ画像は、常にPNGエンコーディングを使用して保存されます。 <span class="varname"> ivalは </span> JPEGの画質(1 ～ 100)を指定します。85以上をお勧めします。 初期設定は <span class="codeph"> -jpegquality 0で、PNG </span>エンコーディングを選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> path </span></span> </p> </td> 
  <td class="stentry"> <p>指定したパス/名前でログファイルを作成します。保存先フォルダに書き込まれたすべての出力ファイルのフルパスが、ログファイルに書き込まれます。また、バージョン情報や発生した警告やエラーなどの追加設定も書き込まれます(詳しくは、 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Output </a> を参照)。 -logを指定しない場合、ログフ <span class="codeph"> ァイルは </span> 作成されません。この場合、すべてのテキスト出力が標準出力に書き込ま <span class="codeph"> れま </span>す。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>vntc処理の優先順位を下 <span class="filepath"> げてく </span> ださい。 ビネットの処理中にvntcがCPU <span class="filepath"> 全体を </span> 引き継がないように、これを使用できます。 オペレーティングシステムが、より重要な他のプロセスにより多くの時間を与えることが可能になります。 <span class="varname"> ivalは、 </span> 優先順位の低い割合(0 ～ 100)を指定します。 初期設定 <span class="codeph"> は —lowerpriority 0 </span>で、vntc処理の優先順位は低くな <span class="filepath"> りま </span> せん。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>vntcが使用できる最大メモ <span class="filepath"> リ量 </span> をバイト単位で指定します。 vntcは、 <span class="filepath"> 最大メ </span> モリ制限に達すると、処理を停止し、エラーを発生させます。 <span class="varname"> ivalは </span> 最大メモリ制限をバイト単位で指定します(0.. 3,758,096,384(3.5 GB)。 ivalが0 <span class="varname"> の場 </span> 合、最大メモリ制限はオフになります。 初期設定は — <span class="codeph"> maxmem 3221225472 </span>です。これは、最大メモリ容量3 GBを意味します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> string </span>" </span> </p> </td> 
  <td class="stentry"> <p>自動生成出力ファイル名のファイル名とサイズ/解像度のサフィックスの間に配置する区切り文字を指定します。 指定しなかった場合、デフォルトは「 — 」です。 destFileまたは <span class="varname"> -infoが指 </span> 定され <span class="codeph"> ている場合は </span> 無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>処理中に再サンプリング（拡大・縮小）された画像へのシャープの適用を有効にします。 キャビネットスタイルのファイルの場合にのみ、サムネールのシャープの適用に適用されます。 </p> <p>シャープを無効にする場合は0（初期設定）、通常のシャープを有効にする場合は1、明るさのみのアンシャープマスクを有効にする場合は2、各カラーコンポーネントのアンシャープマスクを有効にする場合は3を指定します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>ログレベルを設定します。 初期設定は1で、すべての情報、警告およびエラーメッセージを出力します。 0に設定すると、エラーメッセージ以外のすべてのメッセージが無効になります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm量半 <span class="varname"> 径しき </span> い <span class="varname"> 値 — USM量半 </span> 径しき <span class="varname"> い </span> 値 </span> </p> </td> 
  <td class="stentry"> <p>アンシャープマスクのパラメータを設定します。 -sharpenが0ま <span class="codeph"> たは1に設 </span> 定されている場合は無視されます。-sharpenが2ま <span class="codeph"> たは3に設 </span> 定されている場合は必須です。 <span class="varname"> amount </span> は0.0 ～ 500.0の範囲の実数値、 <span class="varname"> radiusは0.0 ～ 10.0の範囲の実数値、 </span> thresholdは0 ～ 255の整数で <span class="varname"></span> す。 詳しくは、『画像サービ <span class="codeph"> ングプロトコルリファ </span> レンス』のop_usm=の説明を参照してください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>特定のビネットが適切な実稼動ビネットであることを検証します。 <span class="varname"> ivalはビネ </span> ットの最小ファイルバージョンを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span></span> </p> </td> 
  <td class="stentry"> <p>出力ファイルのファイルバージョン。 指定する場合は、0または有効なビネットファイルのバージョン（デフォルトのファイルのバージョン以下）である必要があります。 0に設定した場合、または指定しなかった場合、出力ファイルは最新のファイルバージョンを使用して作成されます。 -infoが指定さ <span class="codeph"> れている場合 </span> は無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 ファイル名やその他のオプションを指定しないでください。 </p> </td> 
 </tr> 
</table>

