---
description: sourceFile のタイプに関係なく、次のオプションを適用できます。
solution: Experience Manager
title: 共通オプション
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# 共通オプション{#common-options}

sourceFile のタイプに関係なく、次のオプションを適用できます。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> 文字列 </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルを配置するフォルダー ( <span class="codeph"> -log </span> を指定した場合 )。 絶対パスまたは現在の作業ディレクトリに対する相対パスを指定できます。 フォルダー階層が存在しない場合は作成されます。 で指定されたファイルには適用されません <span class="codeph"> -log </span>. 指定しなかった場合、出力ファイルは <span class="varname"> sourceFile </span> があります。 If <span class="varname"> destFile </span> が指定されている場合、常にその場所に書き込まれ、 <span class="codeph"> -destpath </span> セカンダリ出力ファイルにのみ適用されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -イメージ </span> </p> </td> 
  <td class="stentry"> <p>指定した場合、ビネットから（第 1）ビュー画像を抽出し、キャビネットスタイルから適切なパネル画像を抽出するか、窓カバースタイルの第 1 照明画像を抽出する。 抽出された画像は、フル解像度の画像ファイルとしてTIFFされます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>ターゲットファイルの生成を防ぎます。 から属性をすばやく抽出するのに便利です。 <span class="varname"> sourceFile </span>. オプションのサムネール ( <span class="codeph"> -thumbwidth </span>)，画像 ( <span class="codeph"> -image </span>) およびログファイル ( <span class="codeph"> -log </span>) が生成されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルに埋め込まれたRGBおよびグレースケールの画像データに対して、可逆 PNG ではなく可逆JPEGエンコーディングを選択します。 アルファ (RGBA) を持つ画像は、常に PNG エンコーディングを使用して保存されます。 <span class="varname"> ival </span> JPEG品質を指定します (1...100)。85 以上をお勧めします。 デフォルトはです。 <span class="codeph"> -jpegquality 0 </span>:PNG エンコーディングを選択します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> パス </span> </span> </p> </td> 
  <td class="stentry"> <p>指定されたパス/名前でログファイルを作成します宛先フォルダに書き込まれるすべての出力ファイルの完全なパスは、ログファイルに書き込まれます。また、バージョン情報や警告やエラーなどの追加設定も含まれます ( <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> 出力 </a> を参照 )。 次の場合、ログファイルは作成されません。 <span class="codeph"> -log </span> が指定されていない。この場合、すべてのテキスト出力は <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>優先度を下げる <span class="filepath"> vntc </span> プロセス。 これを使用して、 <span class="filepath"> vntc </span> ビネットの処理中に CPU 全体を引き継ぐことはありません。 これにより、オペレーティングシステムは、より重要な他のプロセスにより多くの時間を割くことができます。 <span class="varname"> ival </span> 優先度の低い割合 (0..100) を指定します。 デフォルトはです。 <span class="codeph"> -lowerpriority 0 </span>: <span class="filepath"> vntc </span> プロセス。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>最大メモリ量を指定します。 <span class="filepath"> vntc </span> はバイト単位で使用できます。 条件 <span class="filepath"> vntc </span> 最大メモリ制限に達すると、処理が停止し、エラーが発生します。 <span class="varname"> ival </span> 最大メモリ制限をバイト単位で指定します (0.. 3,758,096,384(3.5GB)。 条件 <span class="varname"> ival </span> が 0 の場合、最大メモリ制限はオフになります。 デフォルトはです。 <span class="codeph"> -maxmem 3221225472 </span>：最大メモリ容量は 3 GB です。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator " <span class="varname"> 文字列 </span>" </span> </p> </td> 
  <td class="stentry"> <p>自動生成される出力ファイル名のファイル名とサイズ/解像度サフィックスの間に配置する区切り文字を指定します。 指定しない場合のデフォルト値は「 — 」です。 次の場合は無視 <span class="varname"> destFile </span> または <span class="codeph"> -info </span> が指定されている。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> シャープ <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>処理中に再サンプリング（拡大・縮小）された画像のシャープを有効にします。 サムネールのシャープニングは、キャビネットスタイルのファイルの場合にのみ適用されます。 </p> <p>0 を指定するとシャープが無効（デフォルト）になり、1 を指定すると通常のシャープが有効になり、2 を指定すると明るさのみにアンシャープマスクが有効になり、3 を指定すると各カラーコンポーネントにアンシャープマスクが有効になります。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>ログレベルを設定します。 初期設定は 1 で、すべての情報、警告およびエラーメッセージを出力します。 エラーメッセージ以外のすべてのメッセージを無効にするには、0 に設定します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> 量 </span> <span class="varname"> 半径 </span> <span class="varname"> しきい値 </span> </span> </p> </td> 
  <td class="stentry"> <p>アンシャープマスクのパラメーターを設定します。 次の場合は無視 <span class="codeph"> シャープ </span> が 0 または 1 に設定されている場合、必須 <span class="codeph"> シャープ </span> が 2 または 3 に設定されている。 <span class="varname"> 量 </span> は、0.0 ～ 500.0 の範囲の実数です。 <span class="varname"> 半径 </span> は 0.0 ～ 10.0 の範囲の実数値で、 <span class="varname"> しきい値 </span> は 0 ～ 255 の整数です。 詳しくは、 <span class="codeph"> op_usm= </span> （画像サービングプロトコルリファレンス）を参照してください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>特定のビネットが適切な実稼動ビネットであることを検証します。 <span class="varname"> ival </span> ビネットの最小ファイルバージョンを表します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>出力ファイルのファイルバージョン。 指定する場合は、0 または有効なビネットファイルバージョン（デフォルトのファイルバージョン以下）を指定する必要があります。 0 に設定した場合、または指定しなかった場合、出力ファイルは最新のファイルバージョンを使用して作成されます。 次の場合は無視 <span class="codeph"> -info </span> が指定されている。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo </span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 ファイル名やその他のオプションを指定せずに指定します。 </p> </td> 
 </tr> 
</table>
