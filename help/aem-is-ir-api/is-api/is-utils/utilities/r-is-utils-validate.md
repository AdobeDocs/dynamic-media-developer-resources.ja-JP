---
description: 画像検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルが有効であることを確認し、画像サービングが問題なく読み取れることを確認します。
solution: Experience Manager
title: 検証
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
TQID: 'https://experienceleague.adobe.com/gWtVDo3ounZMncdhwLMJsoRaPyZP3E1Fi98L8fX6XFA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 281
ht-degree: 1%

---

# 検証{#validate}

画像検証ユーティリティ。 このコマンドラインユーティリティは、画像ファイルが有効であり、画像サービングで問題なく読み取れることを確認するために画像ファイルを検証します。

PTIFF以外のすべての画像ファイルは、ソースイメージとしてImage Servingでファイルを利用できるようにする前に、検証に合格する必要があります。 PTIFF画像は、信頼性が低い可能性があるコピー操作の後に検証する必要があります。

## 使用方法 {#usage}

` validate *`fileType`* [ *`options`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>Sourceのファイルタイプ。少なくとも1つは指定する必要があります（ – anyは、ICでサポートされている同じ画像ファイルタイプを許可します）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> オプション </span> </span> </p> </td> 
  <td class="stentry"> <p>その他のコマンドオプション（以下を参照）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> ソースファイル </span> </span> </p> </td> 
  <td class="stentry"> <p> 画像ファイル。 スペースで区切られた複数のオブジェクトがない。 </p> </td> 
 </tr> 
</table>

## 返品 {#section-67a7cf7c53144fbb8f24b818f4a10901}

成功した場合は0です。 エラーが発生した場合、ゼロ以外の値が返され、エラーの詳細が`stderr`に送信されます。

## オプション {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>画像ファイルのリストを含む個別のテキストファイルを指定します。 ファイルごとに1 レコード。 <span class="codeph"> -fileList </span>が含まれている場合、<span class="varname"> sourceFile </span>を指定することはできません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>画像ファイル全体の検証を有効にします。 デフォルトでは、画像ヘッダーのみが検証されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>埋め込まれたカラープロファイルの有効性を検証します。 デフォルトでは、ボディプロファイルはチェックされません。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> 画像コンポーネントごとに16 ビットの画像を拒否します。 リモート ソース イメージを検証する際に、常にImage Serverによって指定されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> – 詳細</span> </p> </td> 
  <td class="stentry"> <p> 画像が無効な場合は、詳細な情報を印刷します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> – 無音</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>出力を無効にします。 ステータスのみが返されます。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>追加のファイルがまだ検証されていない場合でも、ファイル検証エラーが発生した場合に処理を終了します。 デフォルトでは、検証エラーが発生すると処理が続行されます </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> – バージョン </span> </p> </td> 
  <td class="stentry"> <p>このユーティリティのバージョン情報を返します。 他のオプションなしで指定します。 </p> </td> 
 </tr> 
</table>
