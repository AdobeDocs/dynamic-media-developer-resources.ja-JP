---
description: イメージ検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルが有効で、画像サービングで読み取りが困難でないことを確認するために画像ファイルを検証します。
seo-description: イメージ検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルが有効で、画像サービングで読み取りが困難でないことを確認するために画像ファイルを検証します。
seo-title: 検証
solution: Experience Manager
title: 検証
topic: Scene7 Image Serving - Image Rendering API
uuid: 87a129ed-950a-4b1a-9240-bf567cd8e38f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 検証{#validate}

イメージ検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルが有効で、画像サービングで読み取りが困難でないことを確認するために画像ファイルを検証します。

PTIFF以外のすべての画像ファイルは、ファイルをソース画像として画像サービングで使用できるようにする前に、検証に合格する必要があります。 PTIFF画像は、信頼性の低いコピー操作の後で検証する必要があります。

## 使用方法 {#usage}

` validate *`FileTypeoptionssourceFile`* [ *``*] [ *``* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ファ <span class="varname"> イルタ </span> イプ </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg| -ptif| -any </span> </p> <p>ソースファイルの種類；少なくとも1つを指定する必要があります（ —anyを指定すると、ICでサポートされているのと同じ画像ファイルタイプを使用できます）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> オプショ </span> ン </span> </p> </td> 
  <td class="stentry"> <p>その他のコマンドオプション（以下を参照）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ソース <span class="varname"> ファ </span> イル </span> </p> </td> 
  <td class="stentry"> <p> 画像ファイル なし（またはスペースで区切られます）。 </p> </td> 
 </tr> 
</table>

## Returns {#section-67a7cf7c53144fbb8f24b818f4a10901}

0（成功した場合） エラーが発生した場合は、ゼロ以外の値が返され、エラーの詳細がに送信されま `stderr`す。

## オプション {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"></span> listFile </span> </p> </td> 
  <td class="stentry"> <p>画像ファイルのリストを含む別のテキストファイルを指定します。 1ファイルにつき1レコード。 -fileListを含 <span class="codeph"> める場 </span> 合は、sourceFile <span class="varname"> を指 </span> 定しないでください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>画像ファイル全体の検証を有効にします。 デフォルトでは、画像ヘッダーのみが検証されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>埋め込まれたカラープロファイルの有効性を検証します。 デフォルトでは、プロファイルボディはチェックされません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> 16ビット/画像コンポーネントの画像を拒否します。 リモートソースイメージを検証する際に、Image Serverによって常に指定されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> 画像が無効な場合に、詳細を印刷します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>stdout <span class="codeph"> / stderr出力を </span>無効に <span class="codeph"></span> します。 ステータスのみが返されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>ファイルの検証エラーが発生した場合、追加のファイルがまだ検証されていない場合でも、処理を終了します。 デフォルトでは、検証エラーが発生しても処理は続行されます </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -バージョン </span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 その他のオプションは使用しないで指定します。 </p> </td> 
 </tr> 
</table>

