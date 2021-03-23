---
description: 'ソフトウェアのインストールに必要な領域に加えて、画像サービングには次のディスク領域の要件があります '
solution: Experience Manager
title: ディスク容量の要件と推奨事項
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '512'
ht-degree: 0%

---


# ディスク容量の要件と推奨事項{#disk-space-requirements-and-recommendations}

ソフトウェアのインストールに必要な領域に加えて、画像サービングには次のディスク領域の要件があります。

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>説明/デフォルトの場所/設定場所</b> </th> 
   <th class="entry"> <b>計算/推奨</b> </th> 
   <th class="entry"> <b>コメント</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>ソース画像、フォント、ICCプロファイル</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>様々です。以下のコメントを参照してください。 </p> </td> 
   <td> <p>Image Serverからのアクセスのみが必要です。サーバーはデータを変更しません。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP応答データキャッシュ</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is-response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2;2 GB以上を推奨。 </p> </td> 
   <td> <p>このキャッシュは、ネスト/埋め込みのデータおよび外部ソース画像も格納します。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>画像カタログのデータキャッシュ</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>カタログフォルダで1.5倍のスペースを使用できるようにします。 </p> </td> 
   <td> <p>カタログが最初に読み込まれたときに設定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>ログデータ</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100Mバイト以上。 </p> </td> 
   <td> <p>ログの設定とサーバーの使用によって異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Image Server一時ファイル</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100 MBは、ほとんどの用途に十分です。 </p> </td> 
   <td> <p>短時間のみ有効なデータ、は、PTIFFや特定の応答画像形式以外のソース画像に必要な場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ソースイメージのディスク領域の要件{#section-317da75099ad480d9a461c7e706d4f1c}

Image Converterコマンドラインツール(IC)を使用して、すべてのソース画像をピラミッド型TIFFファイル形式(PTIFF)に変換することをお勧めします。 この変換により、すべてのアプリケーションに対して画像サービングの最適なランタイムパフォーマンスが確保されます。 Image Serverは、ICが受け入れるすべてのソースファイル形式を処理できますが、Dynamic Mediaは、このような用途をサポートしていません。

PTIFFファイルを使用する場合は、次のサム規則に従って容量の要件を決定できます。

*`total_space`* (bytes) =  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`*)

* *`avg_pixel_count`* すべての元の画像の平均ピクセルサイズ（幅x高さ）。例えば、元の画像が通常2k x 2kピクセル前後である場合、これは4Mピクセルになります。
* *`avg_num_components`* 画像の種類に応じて異なります。ほとんどのRGB画像の場合は3、ほとんどがCMYKまたはRGBA画像の場合は4です。 画像の半分がRGBで、残りの半分がRGBAの場合は3.5を使用します。
* *`p_factor`* 画像をICで変換する際の圧縮タイプと画質の設定によって異なります。

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF圧縮</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>非圧縮 </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0.75（画像に応じて異なります） </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG圧縮 </p> </td> 
   <td> <p> 1（JPEG画質95の場合は標準） </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>この近似値は、ファイルシステムのオーバーヘッドを考慮しません。 ディスク上の実際の領域は、大幅に大きくなる場合があります。

**例**

画像サービングの導入では、平均サイズが500 x 500 RGBピクセルの低解像度のレガシー画像30,000枚を使用する必要があります。 新しい印刷品質の画像データは、年間10,000件の割合で追加される予定です。 通常のCMYK画像サイズは4k x 6kバイトです。 すべてのデータは、高画質でJPEG圧縮されます。 3年間の使用後のディスク領域の合計は、次のように見積もられます。

*`total_space`* = 30,000 x (2k + 0.5k x 0.5k x 3 x 0.1) + 3 x 10,000 x (2k + 4k x 6k x 4 x 0.1) = 2.2 G + 268 GB =約270 GB

最高の品質を保証するために、deflate(zip)圧縮を使用できます。 *`p_factor`*&#x200B;が0.4の場合、必要なディスク領域の合計は約4倍になります。 この場合、1 TBをわずかに超えます。
