---
description: 画像をファイルに保存します。
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---

# saveToFile{#savetofile}

画像をファイルに保存します。

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ファイル</span> </p> </td> 
  <td class="stentry"> <p>ターゲット画像ファイルの相対パス。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>タイムアウト間隔（ミリ秒）。 </p></td> 
 </tr> 
</table>

応答画像をクライアントに返す代わりに、サーバー上のファイルに保存します。

保存リクエストが正常に完了すると、このリクエストは、次のようなJava形式のプロパティを返します。

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> プロパティ</b> </th> 
   <th class="entry"> <b> 種類</b> </th> 
   <th class="entry"> <b> 説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p>ファイル作成時間(1970年1月1日午前0時からのミリ秒数( UTC/GMT)。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 保存する画像のピクセル数。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> enum </p> </td> 
   <td> <p> <span class="codeph"> 成功した場合は</span> done。 </p> </td> 
  </tr> 
 </tbody> 
</table>

リクエストが成功した場合はHTTP応答ステータス200、失敗した場合またはタイムアウトした場合は403を返します。 応答のMIMEタイプが`text/plain`で、キャッシュできません。

重要ファイルへの保存は、`attribute::SavePath`内の既存の書き込み可能なフォルダーへのパスを指定することで有効にする必要があります。 `saveToFile=` が空の場合 `attribute::SavePath` に失敗します。

*`file`* は必須で、と組み合わせた相対パスである必要がありま `attribute::SavePath`す。画像サービングでフォルダーが作成されない。 ターゲットフォルダーがサーバー上に存在し、画像サービングがファイルを作成するための適切な権限設定がある必要があります。

`timeout=` はオプションです。デフォルトのタイムアウトは60,000ミリ秒、または`PS::SaveTimeout`で設定された値です。
