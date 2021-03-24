---
description: 画像をファイルに保存します。
solution: Experience Manager
title: saveToFile
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 3%

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
  <td class="stentry"> <p>タイムアウト間隔（ミリ秒） </p></td> 
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
   <td> <p>ファイル作成時間（1970年1月1日午前0時からのミリ秒数）(UTC/GMT)。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> pixelsTotal</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 保存する画像のピクセル数。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> status</span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> <span class="codeph"> 成功した</span> 場合に実行します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

成功した場合はHTTP応答ステータス200を返し、失敗した場合またはタイムアウトした場合は403を返します。 応答のMIMEタイプが`text/plain`であり、キャッシュできません。

重要ファイルへの保存は、`attribute::SavePath`にある既存の書き込み可能なフォルダーへのパスを指定して有効にする必要があります。 `saveToFile=` が空の場合は失敗 `attribute::SavePath` します。

*`file`* は必須で、と組み合わされる相対パスである必要があり `attribute::SavePath`ます。画像サービングでは、フォルダーは作成されません。 ターゲットフォルダは、サーバに存在し、画像サービングがファイルを作成するための適切な権限設定を持っている必要があります。

`timeout=` はオプションです。デフォルトのタイムアウトは60,000ミリ秒、または`PS::SaveTimeout`で設定されたいずれかの値です。
