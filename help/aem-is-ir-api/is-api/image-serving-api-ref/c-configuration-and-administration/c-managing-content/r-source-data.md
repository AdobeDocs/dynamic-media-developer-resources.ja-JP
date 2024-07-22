---
description: 画像サービングソースファイルには、画像およびマスクファイル、フォント、ICC プロファイルが含まれます。
solution: Experience Manager
title: Source データ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Source データ{#source-data}

画像サービングソースファイルには、画像およびマスクファイル、フォント、ICC プロファイルが含まれます。

すべてのソースデータファイルは、Image Server からアクセスできる必要があります。 画像サービングには、データファイルの場所を指定するための代替手段がいくつか用意されています。

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p>画像サ <span class="codeph"> ビング HTTP リクエストで指定された画像ファイルの相対パスと名前 </span> </p></td> 
 </tr> 
</table>

サーバは、絶対ファイルパスが確立されるまで、パスセグメントを右から左に結合します。

すべての `*`rootPath`*` セグメントは、空、相対、絶対パスセグメントにすることができます。

`*`catalogPath`*` は、絶対ファイルパスまたは相対ファイルパスまたは名前です。 `*`requestPath`*` は、相対ファイルパスまたは相対ファイルパス名である必要があります。

`Multiple IS::RootPath` 値は、ImageServerRegistry.xml で（または管理インターフェイスを介して）定義できます。 これにより、ソース・データ・ファイルを複数のファイル・システムに分散させることができます。 Image Server は、データファイルが見つかるまで、指定された順序で代替パスを試みます。

任意の種類の新しいデータファイルは、サーバーを停止せずにいつでも追加できます。
