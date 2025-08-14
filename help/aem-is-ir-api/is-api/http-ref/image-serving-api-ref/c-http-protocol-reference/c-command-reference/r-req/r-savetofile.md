---
description: 画像をファイルに保存します。
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 1%

---

# saveToFile{#savetofile}

画像をファイルに保存します。

`req=saveToFile&name= *`file`*[&timeout= *`val`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ファイル </span> </p> </td> 
  <td class="stentry"> <p>ターゲット画像ファイルへの相対パス。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>タイムアウト間隔（ミリ秒）。 </p></td> 
 </tr> 
</table>

応答画像をクライアントに返す代わりに、サーバー上のファイルに保存します。

保存リクエストが正常に完了すると、リクエストは、次のような Java 形式のプロパティを返します。

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> プロパティ </b> </th> 
   <th class="entry"> <b> Type</b> </th> 
   <th class="entry"> <b> Description</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p>ファイル作成時間（1970 年 1 月 1 日深夜 0 時からのミリ秒数（UTC/GMT））。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 保存された画像のピクセル数。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> の状態 </span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> 成功 <span class="codeph"> た場合 </span> 完了します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

成功した場合は HTTP 応答ステータス 200、リクエストが失敗またはタイムアウトした場合は 403 を返します。 応答の MIME タイプは `text/plain` で、キャッシュできません。

重要 `attribute::SavePath` の既存の書き込み可能フォルダーへのパスを指定して、ファイルへの保存を有効にする必要があります。 `saveToFile=` が空の場合、`attribute::SavePath` は失敗します。

*`file`* は必須で、`attribute::SavePath` と組み合わされた相対パスである必要があります。 画像サービングでは、フォルダーは作成されません。 ターゲットフォルダーがサーバー上に存在し、画像サービングでファイルを作成するための適切な権限設定を持っている必要があります。

`timeout=` はオプションです。 デフォルトのタイムアウトは 60,000 ミリ秒、または `PS::SaveTimeout` で設定されている値です。
