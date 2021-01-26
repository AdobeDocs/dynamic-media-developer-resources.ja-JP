---
description: sourceFileの種類に関係なく、次のオプションを適用できます。
seo-description: sourceFileの種類に関係なく、次のオプションを適用できます。
seo-title: 一般的なオプション
solution: Experience Manager
title: 一般的なオプション
topic: Dynamic Media Image Serving - Image Rendering API
uuid: fdf09873-4102-4ed6-a315-a87cba5c44c7
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---


# 共通オプション{#common-options}

sourceFileの種類に関係なく、次のオプションを適用できます。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> 文字列  </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルを配置するフォルダー（ログファイルを含む。<span class="codeph"> -log </span>が指定されている場合） 絶対パスまたは現在の作業ディレクトリの相対パスを指定できます。 フォルダー階層が存在しない場合は作成されます。 <span class="codeph"> -log </span>で指定されたファイルには適用されません。 指定しなかった場合、出力ファイルは<span class="varname"> sourceFile </span>が存在するフォルダーに書き込まれます。 <span class="varname"> destFile </span>を指定した場合は、常にその場所に書き込まれ、<span class="codeph"> -destpath </span>はセカンダリ出力ファイルにのみ適用されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -イメージ </span> </p> </td> 
  <td class="stentry"> <p>指定した場合、ビネットから（第1）表示画像、キャビネットスタイルからの適切なパネル画像、または窓覆いスタイルの第1の照明画像から抽出される。 抽出した画像は、最大解像度のTIFFファイルとして保存されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>ターゲットファイルの生成を防ぎます。 <span class="varname"> sourceFile </span>から属性をすばやく抽出するのに役立ちます。 オプションのサムネール(<span class="codeph"> -thumbwidth </span>)、画像(<span class="codeph"> -image </span>)およびログファイル(<span class="codeph"> -log </span>)のみが生成されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルに埋め込まれるRGBおよびグレースケールの画像データに対して、可逆圧縮PNGではなく非可逆圧縮JPEGエンコーディングを選択します。 アルファ(RGBA)を持つ画像は、常にPNGエンコーディングを使用して保存されます。 <span class="varname"> ivalはJPEGの画質(1 ～ 100)を </span> 指定します。85以上をお勧めします。初期設定は<span class="codeph"> -jpegquality 0 </span>で、PNGエンコーディングを選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> パス  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定したパス/名前でログファイルを作成します。宛先フォルダに書き込まれたすべての出力ファイルのフルパスは、ログファイルに書き込まれ、バージョン情報や警告、エラーなどの追加設定が行われます（詳細は<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Output </a>を参照）。 <span class="codeph"> -log </span>が指定されていない場合、ログファイルは作成されません。この場合、すべてのテキスト出力は<span class="codeph"> stdout </span>に書き込まれます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="filepath"> vntc </span>プロセスの優先度を下げます。 これは、ビネットの処理中に<span class="filepath"> vntc </span>がCPU全体を引き継がないようにするために使用できます。 これにより、オペレーティングシステムが、より重要で他のプロセスにより多くの時間を与えることができます。 <span class="varname"> ivalは、優先度の低いパーセント(0 ～ 100)を </span> 指定します。デフォルトは<span class="codeph"> -lowerpriority 0 </span>です。これは<span class="filepath"> vntc </span>プロセスの優先度を下げません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="filepath"> vntc </span>で使用できる最大メモリ量をバイト単位で指定します。 <span class="filepath"> vntc </span>は、メモリの上限に達すると処理を停止し、エラーを発生させます。 <span class="varname"> ivalは、最大メモリ制限をバイト単位で </span> 指定します(0..3,758,096,384(3.5 GB)。 <span class="varname"> ival </span>が0の場合、最大メモリ制限はオフになります。 デフォルトは<span class="codeph"> -maxmem 322125472 </span>で、最大メモリ制限は3 GBです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> 文字列 </span>"  </span> </p> </td> 
  <td class="stentry"> <p>ファイル名と、自動生成出力ファイル名のサイズ/解像度のサフィックスの間に配置する区切り文字を指定します。 指定しない場合、初期設定は「 — 」です。 <span class="varname"> destFile </span>または<span class="codeph"> -info </span>が指定されている場合は無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>処理中にリサンプリング（拡大・縮小）された画像にシャープを適用できるようにします。 キャビネットスタイルのファイルの場合にのみ、サムネールへのシャープの適用に適用されます。 </p> <p>0に設定するとシャープが無効（初期設定）になり、1に設定すると通常のシャープが有効になり、2に設定すると明るさのみのアンシャープマスクが有効になり、3に設定すると各カラーコンポーネントのアンシャープマスクが有効になります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel  </span> </p> </td> 
  <td class="stentry"> <p>ログレベルを設定します。 初期設定は1で、すべての情報、警告およびエラーメッセージを出力します。 エラーメッセージ以外のすべてを無効にするには、0に設定します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> 量 </span> <span class="varname"> 半径 </span> <span class="varname"> しきい値  </span> </span> </p> </td> 
  <td class="stentry"> <p>アンシャープマスクのパラメーターを設定します。 <span class="codeph"> -sharpen </span>が0または1に設定されている場合は無視されます。<span class="codeph"> -sharpen </span>が2または3に設定されている場合は必須です。 <span class="varname"> amount </span> は0.0 ～ 500.0の範囲の実数値で、 <span class="varname"> radius </span> は0.0 ～ 10.0の範囲の実数値で、 <span class="varname"> threshold </span> は0 ～ 255の整数です。詳しくは、『画像サービングプロトコルリファレンス』の「<span class="codeph"> op_usm= </span> 」の説明を参照してください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>特定のビネットが適切な実稼働ビネットであることを検証します。 <span class="varname"> ival </span> は、ビネットの最小ファイルバージョンを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルのファイルのバージョン。 指定する場合、0または有効なビネットファイルのバージョン（初期設定のファイルバージョン以下）を指定する必要があります。 0に設定した場合、または指定しなかった場合、出力ファイルは最新バージョンのファイルを使用して作成されます。 <span class="codeph"> -info </span>が指定されている場合は無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 ファイル名やその他のオプションを指定しないで指定します。 </p> </td> 
 </tr> 
</table>

