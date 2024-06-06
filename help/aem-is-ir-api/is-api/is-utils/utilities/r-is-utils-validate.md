---
description: イメージ検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルが有効であることを確認し、画像サービングで問題なく読み取れるようにします。
solution: Experience Manager
title: 検証
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 1%

---

# 検証{#validate}

イメージ検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルが有効であり、画像サービングで問題なく読み取れるかどうかを確認するために画像ファイルを検証します。

画像サーバーでソース画像としてファイルを利用できるようにするには、すべての非 PTIFF 画像ファイルが検証に合格する必要があります。 信頼性が低い可能性があるコピー操作の後は、PTIFF 画像を検証する必要があります。

## 使用方法 {#usage}

` validate *`fileType`* [ *`オプション`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>ソースファイルのタイプ。少なくとも 1 つを指定する必要があります（– any は、IC でサポートされている同じ画像ファイルタイプを許可します）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> オプション </span> </span> </p> </td> 
  <td class="stentry"> <p>その他のコマンドオプション（後述）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> 画像ファイル。 なし、またはスペースで区切った複数の文字列。 </p> </td> 
 </tr> 
</table>

## 戻り値 {#section-67a7cf7c53144fbb8f24b818f4a10901}

成功した場合は 0 を返します。 エラーが発生した場合は、0 以外の値が返され、エラーの詳細がに送信されます。 `stderr`.

## オプション {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>イメージ ファイルのリストを含むテキスト ファイルを指定します。 ファイルごとに 1 レコード。 次の場合 <span class="codeph"> -fileList </span> 次を含む <span class="varname"> sourceFile </span> を指定しないでください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>画像ファイル全体の検証を有効にします。 デフォルトでは、画像ヘッダーのみが検証されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>埋め込みカラープロファイルが有効かどうかを確認します。 デフォルトでは、本文プロファイルはチェックされません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> 画像コンポーネントあたり 16 ビットの画像を拒否します。 リモート ソース イメージを検証するときに Image Server によって常に指定されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> 画像が無効な場合に詳細情報を出力します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  – サイレント </span> </p> </td> 
  <td class="stentry"> <p>無効 <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span> 出力。 ステータスのみが返されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>追加のファイルがまだ検証されていない場合でも、ファイル検証エラーが発生すると処理を終了します。 デフォルトでは、検証エラーが発生した場合に処理が続行されます </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version </span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 を他のオプションなしで指定します。 </p> </td> 
 </tr> 
</table>
