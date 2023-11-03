---
description: 画像サービングソースデータファイルには、画像ファイルとマスクファイル、フォント、ICC プロファイルが含まれます。
solution: Experience Manager
title: ソースデータ
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# ソースデータ{#source-data}

画像サービングソースデータファイルには、画像ファイルとマスクファイル、フォント、ICC プロファイルが含まれます。

すべてのソースデータファイルは、Image Server からアクセスできる必要があります。 画像サービングには、データファイルの場所を指定するための様々な代替手段が用意されています。

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
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
  <td class="stentry"> <p><span class="codeph"> 画像サービング HTTP 要求で指定された相対的な画像ファイルパスと名前</span> </p></td> 
 </tr> 
</table>

サーバは、絶対ファイルパスが確立されるまで、パスセグメントを右から左に結合します。

すべて `*`rootPath`*` セグメントは、空、相対または絶対パスセグメントのいずれかです。

`*`catalogPath`*` は、絶対または相対ファイルパス/名前です。 `*`requestPath`*` は、相対ファイルパスまたはファイル名である必要があります。

`Multiple IS::RootPath` の値は、ImageServerRegistry.xml（または管理インターフェイスを介して）で定義できます。 これにより、ソース・データ・ファイルを複数のファイル・システムに分散させることができます。 Image Server は、データファイルが見つかるまで、指定された順序で代替パスを試みます。

任意の種類の新しいデータファイルは、サーバーを停止することなく、いつでも追加できます。
