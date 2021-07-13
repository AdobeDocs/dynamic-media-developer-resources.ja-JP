---
description: '画像サービングには、ソフトウェアのインストールに必要な領域に加えて、次のディスク領域要件があります '
solution: Experience Manager
title: ディスク容量の要件と推奨事項
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# ディスク容量の要件と推奨事項{#disk-space-requirements-and-recommendations}

画像サービングには、ソフトウェアのインストールに必要な領域に加えて、次のディスク領域要件があります。

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>説明/デフォルトの場所/で設定</b> </th> 
   <th class="entry"> <b>計算/推奨</b> </th> 
   <th class="entry"> <b>コメント</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>ソース画像、フォント、ICCプロファイル</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>様々です。以下のコメントを参照してください。 </p> </td> 
   <td> <p>Image Serverからのみアクセス可能である必要がある。サーバーがデータを変更することはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP応答データキャッシュ</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is-response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2;2 GB以上を推奨します。 </p> </td> 
   <td> <p>このキャッシュには、ネスト/埋め込みのデータと外部ソース画像も格納されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>画像カタログのデータキャッシュ</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>カタログフォルダーでスペースの1.5倍を使用できるようにします。 </p> </td> 
   <td> <p>カタログが最初に読み込まれると設定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>ログデータ</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100Mバイト以上。 </p> </td> 
   <td> <p>ログの設定とサーバーの使用によって異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Image Serverの一時ファイル</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100 MBは、ほとんどの用途で十分です。 </p> </td> 
   <td> <p>短時間のみ有効なデータは、PTIFFや特定の応答画像形式以外のソース画像に必要な場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ソースイメージのディスク容量の要件 {#section-317da75099ad480d9a461c7e706d4f1c}

画像コンバーターコマンドラインツール(IC)を使用して、すべてのソース画像をピラミッドTIFFファイル形式(PTIFF)に変換することをお勧めします。 この変換により、すべてのアプリケーションに対して画像サービングの最適なランタイムパフォーマンスが実現します。 Image Serverは、ICが受け入れるすべてのソースファイル形式を処理できますが、Dynamic Mediaはこのような使用をサポートしていません。

PTIFFファイルを使用する場合、次のサムのルールがスペース要件の判断に役立ちます。

*`total_space`* （バイト） =  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`*)

* *`avg_pixel_count`* すべての元のソース画像の平均ピクセルサイズ（幅x高さ）。例えば、元の画像が通常2k x 2kピクセル前後の場合、これは4Mピクセルになります。
* *`avg_num_components`* 画像の種類に応じて異なります。ほとんどのRGB画像の場合は3、ほとんどがCMYKまたはRGBA画像の場合は4です。 画像の半分がRGBで、残りの半分がRGBAの場合は3.5を使用します。
* *`p_factor`* 画像がICで変換される際の圧縮タイプと画質の設定に依存します。

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
   <td> <p>デフレート — 圧縮 </p> </td> 
   <td> <p> 25～0.75（画像に応じる） </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG圧縮 </p> </td> 
   <td> <p> 1（JPEG画質95で典型的） </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>この近似は、ファイルシステムのオーバーヘッドを考慮しません。 ディスク上の実際の領域は、大幅に大きくなる場合があります。

**例**

画像サービングの導入では、30,000個の低解像度のレガシー画像を使用し、平均サイズは500 x 500 RGBピクセルにする必要があります。 新しい印刷品質の画像データは、年間10,000件の割合で追加される予定です。 一般的なCMYK画像サイズは4 KB x 6 KBです。 すべてのデータは、高品質でJPEG圧縮されます。 3年間の使用後のディスク容量の合計は、次のように見積もられます。

*`total_space`* = 30,000 x (2k + 0.5k x 0.5k x 3 x 0.1) + 3 x 10,000 x (2k + 4k x 6k x 4 x 0.1) = 2.2 G + 268 GB =約270 GB

最高の品質を保証するために、deflate(zip)圧縮を使用できます。 *`p_factor`*&#x200B;が0.4の場合、必要なディスク領域の合計は約4倍になります。 この場合、1 TBをわずかに超えます。
