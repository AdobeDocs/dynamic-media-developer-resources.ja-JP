---
description: 画像検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルが有効であること、および画像サービングで簡単に読み取れることを確認するために画像ファイルを検証します。
seo-description: 画像検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルが有効であること、および画像サービングで簡単に読み取れることを確認するために画像ファイルを検証します。
seo-title: 検証
solution: Experience Manager
title: 検証
topic: Scene7 Image Serving - Image Rendering API
uuid: 87a129ed-950a-4b1a-9240-bf567cd8e38f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 1%

---


# 検証{#validate}

画像検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルが有効であること、および画像サービングで簡単に読み取れることを確認するために画像ファイルを検証します。

PTIFF以外のすべての画像ファイルは、ファイルをソース画像として画像サービングで使用できるようにする前にvalidateを渡す必要があります。 PTIFF画像は、信頼性の低いコピー操作の後で検証する必要があります。

## 使用方法 {#usage}

` validate *``* [ *``*] [ *`fileTypeoptionssourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any  </span> </p> <p>ソースファイルの種類；少なくとも1つを指定する必要があります（ —anyを指定すると、ICでサポートされるのと同じ画像ファイルタイプを使用できます）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> options  </span> </span> </p> </td> 
  <td class="stentry"> <p>その他のコマンドオプション（以下を参照）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> 画像ファイル なし（またはそれ以上）。スペースで区切ります。 </p> </td> 
 </tr> 
</table>

## {#section-67a7cf7c53144fbb8f24b818f4a10901}を返す

成功した場合は0。 エラーが発生した場合は、ゼロ以外の値が返され、エラーの詳細が`stderr`に送信されます。

## オプション {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>画像ファイルのリストを含む別のテキストファイルを指定します。 1ファイルにつき1レコード。 <span class="codeph"> -fileList </span>を含める場合、<span class="varname"> sourceFile </span>を指定しないでください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>画像ファイル全体の検証を有効にします。 デフォルトでは、イメージヘッダーのみが検証されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>埋め込まれたカラープロファイルの有効性を検証します。 デフォルトでは、プロファイルの本文はチェックされません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> 16ビット/画像コンポーネントの画像を拒否します。 リモートソースイメージを検証するときに、Image Serverによって常に指定されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> 画像が無効な場合に、より多くの情報を印刷します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>出力を無効にします。 ステータスのみが返されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>ファイルの検証エラーが発生した場合に、まだ検証されていないファイルがあっても処理を終了します。 デフォルトでは、検証エラーが発生しても処理は続行されます </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -バージョン </span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 他のオプションは使用しないで指定します。 </p> </td> 
 </tr> 
</table>

