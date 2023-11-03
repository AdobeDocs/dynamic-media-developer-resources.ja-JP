---
description: 画像の検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルを検証して、画像ファイルが有効であり、画像サービングによって簡単に読み取れることを確認します。
solution: Experience Manager
title: 検証
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---

# 検証{#validate}

画像の検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルを検証して、画像ファイルが有効であり、画像サービングによって簡単に読み取れることを確認します。

PTIFF 以外のすべての画像ファイルが検証を受け取った後で、ファイルがソース画像として画像サービングで使用できるようにする必要があります。 PTIFF 画像は、信頼性の低いコピー操作の後に検証する必要があります。

## 使用方法 {#usage}

` validate *`fileType`* [ *`options`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>ソースファイルタイプ。少なくとも 1 つを指定する必要があります（ —any を使用すると、IC でサポートされる同じ画像ファイルタイプが許可されます）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> options </span> </span> </p> </td> 
  <td class="stentry"> <p>その他のコマンドオプション（以下を参照）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> 画像ファイル。 なし（または複数）（スペースで区切る）。 </p> </td> 
 </tr> 
</table>

## 戻り値 {#section-67a7cf7c53144fbb8f24b818f4a10901}

成功した場合は 0。 エラーが発生した場合は、ゼロ以外の値が返され、エラーの詳細が `stderr`.

## オプション {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>画像ファイルのリストを含む別のテキストファイルを指定します。 1 ファイルにつき 1 レコード。 次の場合 <span class="codeph"> -fileList </span> が含まれている場合、 <span class="varname"> sourceFile </span> は指定できません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>画像ファイル全体の検証を有効にします。 デフォルトでは、画像ヘッダーのみが検証されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>埋め込まれたカラープロファイルが有効かどうかを確認します。 デフォルトでは、プロファイル本文はチェックされていません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> 画像コンポーネントあたり 16 ビットの画像を拒否します。 リモートソースイメージを検証する際に Image Server で常に指定されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> 画像が無効な場合は、詳細情報を出力します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>無効 <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span> 出力。 ステータスのみが返されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>追加のファイルがまだ検証されていない場合でも、ファイルの検証エラーが発生すると処理を終了します。 デフォルトでは、検証エラーが発生した場合も処理は続行されます </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -バージョン </span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 他のオプションは指定しないでください。 </p> </td> 
 </tr> 
</table>
