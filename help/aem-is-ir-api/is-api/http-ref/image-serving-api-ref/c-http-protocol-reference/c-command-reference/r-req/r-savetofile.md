---
description: 画像をファイルに保存します。
seo-description: 画像をファイルに保存します。
seo-title: saveToFile
solution: Experience Manager
title: saveToFile
topic: Scene7 Image Serving - Image Rendering API
uuid: 32a56d77-89e2-4f78-9fab-1b528e9a024a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# saveToFile{#savetofile}

画像をファイルに保存します。

`req=saveToFile&name= *``*[&timeout= *`fileval`*]`

<table id="simpletable_5674FD9655FE4CDDB0E5DC8655890A66"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ファイル</span> </p> </td> 
  <td class="stentry"> <p>ターゲット画像ファイルの相対パス </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p></td> 
  <td class="stentry"> <p>タイムアウト間隔（ミリ秒）。 </p></td> 
 </tr> 
</table>

応答画像をクライアントに返す代わりに、サーバー上のファイルに保存します。

保存要求が正常に完了すると、次のようなJava形式のプロパティが返されます。

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
   <td> <p>ファイル作成時刻(1970年1月1日午前0時からのミリ秒数(UTC/GMT))。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 保存した画像のピクセル数。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> <span class="codeph"> 成功した場合は</span> 、完了します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

成功した場合はHTTP応答ステータス200を返し、失敗またはタイムアウトした場合は403を返します。 応答にMIMEタイプが含まれており、キャ `text/plain` ッシュできません。

重要ファイルへの保存は、にある既存の書き込み可能なフォルダーのパスを指定して有効にする必要がありま `attribute::SavePath`す。 `saveToFile=` が空の場合は失 `attribute::SavePath` 敗します。

*`file`* は必須で、と組み合わされる相対パスである必要がありま `attribute::SavePath`す。 画像サービングでは、フォルダは作成されません。 対象フォルダは、サーバ上に存在し、画像サービングでファイルを作成するための適切な権限設定を持っている必要があります。

`timeout=` はオプションです。 デフォルトのタイムアウトは60,000ミリ秒です。どちらかの値を使用して設定する必要がありま `PS::SaveTimeout`す。
