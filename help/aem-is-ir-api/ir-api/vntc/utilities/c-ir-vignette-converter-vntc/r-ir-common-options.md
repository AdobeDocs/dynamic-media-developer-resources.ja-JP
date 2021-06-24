---
description: sourceFileのタイプに関係なく、次のオプションを適用できます。
solution: Experience Manager
title: 共通オプション
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# 共通オプション{#common-options}

sourceFileのタイプに関係なく、次のオプションを適用できます。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath文 <span class="varname"> 字列  </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルを配置するフォルダー（<span class="codeph"> -log </span>が指定されている場合は、ログファイルを含む）。 絶対パスまたは現在の作業ディレクトリの相対パスを指定できます。 フォルダー階層が存在しない場合は作成されます。 <span class="codeph"> -log </span>で指定されたファイルには適用されません。 指定しなかった場合、出力ファイルは<span class="varname"> sourceFile </span>が存在するフォルダーに書き込まれます。 <span class="varname"> destFile </span>を指定した場合は、常にその場所に書き込まれ、 <span class="codeph"> -destpath </span>はセカンダリ出力ファイルにのみ適用されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -イメージ </span> </p> </td> 
  <td class="stentry"> <p>指定された場合、ビネットから（第1）のビュー画像を抽出し、キャビネットスタイルから適切なパネル画像を抽出するか、窓覆いスタイルの第1の照明画像を抽出する。 抽出された画像は、フル解像度のTIFFファイルとして保存されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>ターゲットファイルの生成を防ぎます。 <span class="varname"> sourceFile </span>から属性をすばやく抽出するのに役立ちます。 オプションのサムネール( <span class="codeph"> -thumbwidth </span> )、画像( <span class="codeph"> -image </span> )およびログファイル( <span class="codeph"> -log </span> )のみが生成されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルに埋め込まれるRGBおよびグレースケールの画像データに対して、可逆PNGではなく非可逆JPEGエンコーディングを選択します。 アルファ(RGBA)を持つ画像は、常にPNGエンコーディングを使用して保存されます。 <span class="varname"> ivalは </span> JPEG画質(1 ～ 100)を指定します。85以降をお勧めします。初期設定は<span class="codeph"> -jpegquality 0 </span>で、PNGエンコーディングを選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log  <span class="varname"> path  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定されたパス/名前を持つログファイルを作成します。宛先フォルダに書き込まれるすべての出力ファイルの完全なパスに加え、バージョン情報や発生した警告やエラーなどの追加設定がログファイルに書き込まれます（詳しくは<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Output </a>を参照）。 <span class="codeph"> -log </span>が指定されていない場合、ログファイルは作成されません。この場合、すべてのテキスト出力は<span class="codeph"> stdout </span>に書き込まれます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="filepath"> vntc </span>プロセスの優先順位を下げます。 これは、ビネットの処理中に<span class="filepath"> vntc </span>がCPU全体を引き継がないようにするために使用できます。 オペレーティングシステムは、より重要な他のプロセスにより多くの時間を与えることができます。 <span class="varname"> ival </span> は、優先度の低い割合(0 ～ 100)を指定します。初期設定は<span class="codeph"> -lowerpriority 0 </span>で、<span class="filepath"> vntc </span>プロセスの優先度を低くしません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="filepath"> vntc </span>が使用できるメモリの最大量をバイト単位で指定します。 <span class="filepath"> vntc </span>が最大メモリ制限に達すると、処理が停止し、エラーが発生します。 <span class="varname"> ival </span> は、最大メモリ制限をバイト単位(0..3,758,096,384(3.5GB))。 <span class="varname"> ival </span>が0の場合、最大メモリ制限はオフになります。 初期設定は<span class="codeph"> -maxmem 3221225472 </span>で、最大メモリ制限は3 GBです。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator "  <span class="varname"> string  </span>"  </span> </p> </td> 
  <td class="stentry"> <p>ファイル名と、自動生成される出力ファイル名のサイズ/解像度のサフィックスとの間に配置する区切り文字を指定します。 指定しない場合は、デフォルトで「 — 」が使用されます。 <span class="varname"> destFile </span>または<span class="codeph"> -info </span>が指定されている場合は無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — シャープ <span class="varname"> 値  </span> </span> </p> </td> 
  <td class="stentry"> <p>処理中に再サンプリング（拡大/縮小）された画像のシャープを有効にします。 キャビネットスタイルのファイルの場合にのみ、サムネールのシャープニングに適用されます。 </p> <p>シャープを無効にする場合は0を指定し、通常のシャープを有効にする場合は1を指定し、明るさのみの場合は2を指定し、各カラーコンポーネントの場合は3を指定します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel  </span> </p> </td> 
  <td class="stentry"> <p>ログレベルを設定します。 初期設定は1で、すべての情報、警告およびエラーメッセージを出力します。 エラーメッセージ以外のすべてを無効にするには、0に設定します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm量半 <span class="varname"> 径し </span> <span class="varname"> きい </span> <span class="varname"> 値  </span> </span> </p> </td> 
  <td class="stentry"> <p>アンシャープマスクのパラメーターを設定します。 <span class="codeph"> -sharpen </span>が0または1に設定されている場合は無視されます。<span class="codeph"> -sharpen </span>が2または3に設定されている場合は必須です。 <span class="varname"> amount </span> は、0.0 ～ 500.0の範囲の実数値、  <span class="varname"> radius </span> は0.0 ～ 10.0の範囲の実数値、  <span class="varname"> threshold </span> は0 ～ 255の整数です。詳しくは、画像サービングプロトコルリファレンスの<span class="codeph"> op_usm= </span>の説明を参照してください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>特定のビネットが適切な実稼動ビネットであることを検証します。 <span class="varname"> ival </span> は、ビネットの最小ファイルバージョンを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルのファイルバージョン。 指定する場合は、0または有効なビネットファイルバージョン（デフォルトのファイルバージョン以下）を指定する必要があります。 0に設定した場合、または指定しなかった場合、出力ファイルは最新のファイルバージョンを使用して作成されます。 <span class="codeph"> -info </span>が指定されている場合は無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 ファイル名やその他のオプションを指定せずに指定します。 </p> </td> 
 </tr> 
</table>
