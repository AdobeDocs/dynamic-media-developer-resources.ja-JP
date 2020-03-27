---
description: 画像サービングのソースデータファイルには、画像ファイル、マスクファイル、フォント、ICCプロファイルが含まれます。
seo-description: 画像サービングのソースデータファイルには、画像ファイル、マスクファイル、フォント、ICCプロファイルが含まれます。
seo-title: ソースデータ
solution: Experience Manager
title: ソースデータ
topic: Scene7 Image Serving - Image Rendering API
uuid: d654eee7-ef2d-4546-93bb-72f80c38e018
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ソースデータ{#source-data}

画像サービングのソースデータファイルには、画像ファイル、マスクファイル、フォント、ICCプロファイルが含まれます。

すべてのソースデータファイルは、Image Serverからアクセスできる必要があります。 画像サービングには、データファイルの場所を指定するための様々な代替オプションが用意されています。

` *`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> rootPath <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> filePath <span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalog <span class="varname"> Path</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> Request <span class="varname"> Path</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> 画像サービングHTTP要求で指定された相対画像ファイルのパスと名前</span> </p></td> 
 </tr> 
</table>

サーバは、絶対ファイルパスが確立されるまで、右から左へのパスセグメントを結合します。

すべての ` *`rootPath`*` セグメントは、空、相対、または絶対パスセグメントにすることができます。

` *`catalogPathは`*` 、絶対パスまたは相対ファイルパス/ファイル名です。 ` *`requestPathは`*` 、相対ファイルパスまたはファイル名で指定する必要があります。

`Multiple IS::RootPath` の値は、ImageServerRegistry.xmlで（または管理インターフェイスを使用して）定義できます。 これにより、複数のファイル・システムにソース・データ・ファイルを配布できます。 Image Serverは、データファイルが見つかるまで、指定された順序で代替パスを試みます。

任意の種類の新しいデータファイルを、サーバーを停止しなくてもいつでも追加できます。
