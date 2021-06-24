---
description: 画像検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルを検証して、画像ファイルが有効であり、画像サービングで簡単に読み取れることを確認します。
solution: Experience Manager
title: 検証
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---

# 検証{#validate}

画像検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルを検証して、画像ファイルが有効であり、画像サービングで簡単に読み取れることを確認します。

PTIFF以外のすべての画像ファイルは、ファイルがソース画像として画像サービングで使用できるようになる前に、検証に合格する必要があります。 PTIFF画像は、信頼性の低いコピー操作の後に検証する必要があります。

## 使用方法 {#usage}

` validate *``* [ *``*] [ *`fileTypeoptionssourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any  </span> </p> <p>ソースファイルタイプ少なくとも1つを指定する必要があります（ —anyを使用すると、ICでサポートされるのと同じ画像ファイルタイプが許可されます）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> options  </span> </span> </p> </td> 
  <td class="stentry"> <p>その他のコマンドオプション（以下を参照）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> 画像ファイル。 なし（またはスペースで区切られた値） </p> </td> 
 </tr> 
</table>

## 戻り値 {#section-67a7cf7c53144fbb8f24b818f4a10901}

成功した場合は0。 エラーが発生した場合は、ゼロ以外の値が返され、エラーの詳細が`stderr`に送信されます。

## オプション {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>画像ファイルのリストを含む別のテキストファイルを指定します。 1ファイルにつき1レコード。 <span class="codeph"> -fileList </span>を含める場合は、<span class="varname"> sourceFile </span>を指定しないでください。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>画像ファイル全体の検証を有効にします。 デフォルトでは、画像ヘッダーのみ検証されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>埋め込みカラープロファイルが有効かどうかを確認します。 デフォルトでは、プロファイルボディはチェックされません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> 16ビット/画像コンポーネントを含む画像を拒否します。 リモートソースイメージを検証する場合、Image Serverで常に指定されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> イメージが無効な場合は、さらに多くの情報を出力します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent  </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>出力を無効にします。 ステータスのみが返されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>追加のファイルがまだ検証されていない場合でも、ファイルの検証エラーが発生すると処理を終了します。 デフォルトでは、検証エラーが発生すると処理は続行されます </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -バージョン </span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 他のオプションは指定しないでください。 </p> </td> 
 </tr> 
</table>
