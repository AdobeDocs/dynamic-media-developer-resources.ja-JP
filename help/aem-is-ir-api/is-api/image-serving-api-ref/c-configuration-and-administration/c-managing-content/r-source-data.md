---
description: 画像ソースデータファイルには、画像およびマスクファイル、フォント、ICC プロファイルが含まれます。
solution: Experience Manager
title: Source data
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
TQID: 'https://experienceleague.adobe.com/36EvEOjHZ8ik-gps-vaap5PhFCf5rwV9ecfkKHZcIhk'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 0%

---

# Source data{#source-data}

画像ソースデータファイルには、画像およびマスクファイル、フォント、ICC プロファイルが含まれます。

すべてのソースデータファイルには、Image Serverからアクセスできる必要があります。 画像サービングには、データファイルの場所を指定するための多くの代替手段が用意されています。

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">は：:RootPath/attribute::RootPath</span>です </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> カタログ：：パス|カタログ：:MaskPath|icc::ProfilePath|フォント：:FontPath|フォント：:MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">画像サービング HTTP リクエストで指定された相対イメージ ファイルのパスと名前</span> </p></td> 
 </tr> 
</table>

サーバーは、絶対ファイルパスが確立されるまで、パスセグメントを右から左に結合します。

すべての`*`rootPath`*` セグメントは、空、相対、または絶対パスセグメントにすることができます。

`*`catalogPath`*`は、絶対または相対ファイルパス/名前です。 `*`requestPath`*`は相対ファイルパス/名前である必要があります。

`Multiple IS::RootPath`個の値は、ImageServerRegistry.xmlで（または管理インターフェイスを使用して）定義できます。 これにより、ソースデータファイルを複数のファイルシステムに分散させることができます。 Image Serverは、データファイルが見つかるまで、指定された順序で代替パスを試みます。

サーバーを停止することなく、いつでも任意の種類の新しいデータファイルを追加できます。
