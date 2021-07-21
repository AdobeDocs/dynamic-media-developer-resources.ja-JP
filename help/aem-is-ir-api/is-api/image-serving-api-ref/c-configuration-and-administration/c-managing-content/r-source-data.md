---
description: 画像サービングのソースデータファイルには、画像ファイルとマスクファイル、フォント、ICCプロファイルが含まれます。
solution: Experience Manager
title: ソースデータ
feature: Dynamic Media Classic、SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# ソースデータ{#source-data}

画像サービングのソースデータファイルには、画像ファイルとマスクファイル、フォント、ICCプロファイルが含まれます。

すべてのソースデータファイルは、Image Serverからアクセスできる必要があります。 画像サービングには、データファイルの場所を指定するための様々な代替手段が用意されています。

`*`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 画像サービングHTTP要求で指定された相対画像ファイルパスと名前</span> </p></td> 
 </tr> 
</table>

サーバは、絶対ファイルパスが確立されるまで、パスセグメントを右から左に結合します。

すべての`*`rootPath`*`セグメントは、空、相対、または絶対パスセグメントにすることができます。

`*``*` catalogPath絶対または相対ファイルパス/名前。`*``*` requestPathは、相対ファイルパスまたは相対ファイル名にする必要があります。

`Multiple IS::RootPath` の値は、 ImageServerRegistry.xmlで（または管理インターフェイスを使用して）定義できます。これにより、ソース・データ・ファイルを複数のファイル・システムに分散できます。 Image Serverは、データファイルが見つかるまで、指定された順序で代替パスを試みます。

任意の種類の新しいデータファイルは、サーバーを停止することなくいつでも追加できます。
