---
title: 共通オプション
description: 次のオプションは、sourceFile のタイプに関係なく適用できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# 共通オプション{#common-options}

次のオプションは、sourceFile のタイプに関係なく適用できます。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> 文字列 </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルを配置するフォルダ（– log <span class="codeph"> が指定されてい </span> 場合はログ・ファイルを含む）。 絶対パスまたは現在の作業ディレクトリへの相対パスを指定できます。 フォルダー階層は存在しない場合は作成されますが、-log <span class="codeph"> で指定したファイル </span> は適用されません。 指定しない場合、出力ファイルは <span class="varname"> sourceFile フ </span> イルが配置されているフォルダーに書き込まれます。 destFile <span class="varname"> が指定され </span> いる場合は、常にその場所に書き込まれ、-destpath <span class="codeph"></span> セカンダリ出力ファイルにのみ適用されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> – 画像 </span> </p> </td> 
  <td class="stentry"> <p>指定した場合、（最初の）ビューイメージがビネットから抽出され、適切なパネル イメージがキャビネット スタイルから抽出され、ウィンドウのカバースタイルの最初のイルミネーション イメージが抽出されます。 抽出された画像は、フル解像度のTIFF ファイルとして保存されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>ターゲットファイルを生成できないようにします。 <span class="varname"> sourceFile フ </span> イルから属性をすばやく抽出する場合に役立ちます。 オプションのサムネール（<span class="codeph"> -thumbwidth </span>）、画像（<span class="codeph"> -image </span>）、ログファイル（<span class="codeph"> -log </span>）のみが生成されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルに埋め込まれたRGBおよびグレースケール画像データに対して、可逆圧縮 PNG ではなく、非可逆圧縮JPEG エンコーディングを選択します。 アルファ版（RGBA）の画像は、常に PNG エンコーディングを使用して保存されます。 ival <span class="varname"></span>、JPEGの画質（1...100）を指定します。85 以上を指定することをお勧めします。 デフォルトは <span class="codeph"> -jpegquality 0 </span> で、PNG エンコーディングが選択されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> path </span> </span> </p> </td> 
  <td class="stentry"> <p>指定されたパス/名前でログ ファイルを作成します。 出力先フォルダーに書き込まれるすべての出力ファイルの完全パスがログファイルおよび一部の追加設定（バージョン情報や発生した警告またはエラーなど）に書き込まれます（詳しくは、<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Output </a> を参照してください）。 -log <span class="codeph"> が指定されていない場合 </span> ログファイルは作成されません。この場合、すべてのテキスト出力が <span class="codeph"> の stdout </span> に書き込まれます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p><span class="filepath"> vntc </span> プロセスの優先順位を下げます。 このプロセスは、ヴィネットの処理中 <span class="filepath">vntc </span> がCPU全体を占有しないように使用できます。 これにより、オペレーティングシステムは他のより重要なプロセスにより多くの時間を与えることができます。 <span class="varname"></span> は、優先度の低い方の割合を指定します（0..100）。 デフォルトは <span class="codeph"> -lowerpriority 0 </span> で、<span class="filepath"> vntc </span> プロセスの優先順位は下がりません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>vntc <span class="filepath"> ーバーが使用できるメモリ </span> 最大量をバイト単位で指定します。 vntc <span class="filepath"></span> 最大メモリ制限に達すると、処理が停止し、エラーが発生します。 <span class="varname"> ival </span> は、最大メモリ制限をバイト （0.. 3,758,096,384 （3.5 GB））。 ival <span class="varname"> が 0</span> 場合、最大メモリ制限はオフになります。 デフォルトは <span class="codeph"> -maxmem 3221225472 </span> です。これは、最大メモリ制限が 3 GB であることを意味します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> string </span>" </span> </p> </td> 
  <td class="stentry"> <p>自動生成された出力ファイル名について、ファイル名とサイズ/解像度の接尾辞の間に配置する区切り文字を指定します。 指定しない場合のデフォルトは「–」です。 destFile <span class="varname"> または </span> -info <span class="codeph"> が指定されてい </span> 場合は無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>処理中に再サンプリング（拡大/縮小）された画像のシャープニングを有効にします。 キャビネットスタイルのファイルのサムネールのシャープニングにのみ適用されます。 </p> <p>シャープを無効にする場合は 0 （デフォルト）、通常のシャープを有効にする場合は 1、明るさのみのアンシャープマスクを有効にする場合は 2、色の各成分のアンシャープマスクを有効にする場合は 3 を指定します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>ログレベルを設定します。 デフォルトは 1 で、すべての情報、警告、およびエラーメッセージが出力されます。 0 に設定すると、エラーメッセージ以外はすべて無効になります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> 半径 </span><span class="varname"></span> しきい値 <span class="varname"></span> </span> </p> </td> 
  <td class="stentry"> <p>アンシャープマスクのパラメータを設定します。 -sharpen <span class="codeph"></span>0 または 1 に設定されている場合は無視されます。-sharpen <span class="codeph"></span>2 または 3 に設定されている場合は必須です。 <span class="varname"> 量 </span> は 0.0～500.0 の範囲の実数値、<span class="varname"> 半径 </span> は 0.0～10.0 の範囲の実数値、<span class="varname"> しきい値 </span> は 0～255 の整数です。 詳しくは <span class="codeph"> 画像サービングプロトコルリファレンスの op_usm= </span> の説明を参照してください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>指定したビネットが適切な実稼動ビネットであることを検証します。 <span class="varname"> ival </span> は、ビネットの最小ファイルバージョンを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルのファイルバージョン。 指定する場合は、0 または有効なヴィネットファイルバージョン （デフォルトのファイルバージョンを超えない）にする必要があります。 0 に設定した場合、または指定しなかった場合、出力ファイルは最新のファイル バージョンを使用して作成されます。 -info <span class="codeph"> が指定され </span> いる場合は無視されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 ファイル名および他のオプションを指定せずに指定します。 </p> </td> 
 </tr> 
</table>
