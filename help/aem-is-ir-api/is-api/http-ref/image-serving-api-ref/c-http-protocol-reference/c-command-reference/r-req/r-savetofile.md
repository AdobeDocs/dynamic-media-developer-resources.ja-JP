---
description: 画像をファイルに保存
solution: Experience Manager
title: saveToFile
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 10a8ea5c-7e64-4d99-a263-779f08ea6e37
TQID: 'https://experienceleague.adobe.com/6JtqM7IKcYInFZ4zyuAIVwOabdXIltB2ZsVZP6pLL4E'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 184
ht-degree: 1%

---

# saveToFile{#savetofile}

画像をファイルに保存

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

応答イメージをクライアントに返す代わりに、サーバー上のファイルに保存します。

保存リクエストが正常に完了すると、リクエストは次のようなJava形式のプロパティを返します。

<table id="table_8BA8F75A0B7241BAB9B4359F97C21137"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> プロパティ </b> </th> 
   <th class="entry"> <b> タイプ </b> </th> 
   <th class="entry"> <b>説明</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> lastUpdated</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p>ファイルの作成時間（1970年1月1日深夜0時からのミリ秒数）。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ピクセル合計</span> </p> </td> 
   <td> <p> 整数 </p> </td> 
   <td> <p> 保存された画像内のピクセル数。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> ステータス </span> </p> </td> 
   <td> <p> 列挙 </p> </td> 
   <td> <p> <span class="codeph">が成功した場合は</span>を完了しました。 </p> </td> 
  </tr> 
 </tbody> 
</table>

HTTP応答ステータスを返します。正常な場合は200、リクエストが失敗またはタイムアウトした場合は403。 応答はMIME タイプ `text/plain`を持ち、キャッシュできません。

重要`attribute::SavePath`で既存の書き込み可能フォルダーへのパスを指定して、ファイルへの保存を有効にする必要があります。 `attribute::SavePath`が空の場合、`saveToFile=`は失敗します。

*`file`*&#x200B;は必須であり、`attribute::SavePath`と組み合わされた相対パスである必要があります。 画像サービングでフォルダーが作成されない。 ターゲットフォルダーはサーバーに存在し、画像サービングでファイルを作成するための適切な権限設定が必要です。

`timeout=`はオプションです。 デフォルトのタイムアウトは60,000 ミリ秒、または`PS::SaveTimeout`で設定された値のいずれかです。
