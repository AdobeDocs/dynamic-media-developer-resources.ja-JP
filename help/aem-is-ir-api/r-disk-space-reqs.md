---
description: '画像サービングには、ソフトウェアのインストールに必要な容量に加え、次のディスク容量要件があります '
solution: Experience Manager
title: ディスク容量の要件と推奨事項
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 0%

---

# ディスク容量の要件と推奨事項{#disk-space-requirements-and-recommendations}

画像サービングには、ソフトウェアのインストールに必要な容量に加え、次のディスク容量要件があります。

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>説明/デフォルトの場所/次で設定</b> </th> 
   <th class="entry"> <b>計算/レコメンデーション</b> </th> 
   <th class="entry"> <b>コメント</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>ソース画像、フォント、ICC プロファイル</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>様々下のコメントを参照してください。 </p> </td> 
   <td> <p>Image Server からのアクセスのみが必要です。サーバーがデータを変更することはありません。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP 応答データキャッシュ</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2;2 GB 以上を推奨します。 </p> </td> 
   <td> <p>このキャッシュには、ネストされた/埋め込まれたデータと外部ソース画像も格納されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>画像カタログのデータキャッシュ</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>カタログフォルダーでスペースを 1.5 倍にします。 </p> </td> 
   <td> <p>カタログが最初に読み込まれるときに設定されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>ログデータ</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100M バイト以上。 </p> </td> 
   <td> <p>ログの設定とサーバーの使用に応じて異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Image Server の一時ファイル</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>ほとんどの用途には 100 MB で十分です。 </p> </td> 
   <td> <p>短時間のみ有効なデータは、PTIFF 以外のソース画像や特定の応答画像形式に必要な場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ソースイメージのディスク容量の要件 {#section-317da75099ad480d9a461c7e706d4f1c}

画像コンバーターコマンドラインツール (IC) を使用して、すべてのソース画像をピラミッドTIFFファイル形式 (PTIFF) に変換することをお勧めします。 この変換により、すべてのアプリケーションに対して画像サービングの最適なランタイムパフォーマンスが実現します。 Image Server は、IC で受け入れられるすべてのソースファイル形式を処理できますが、Dynamic Mediaはこのような使用をサポートしていません。

PTIFF ファイルを使用する場合、次のサムの規則が必要なスペースを判断するのに役立ちます。

*`total_space`* （バイト） = *`number_of_images`* x(2000 + *`avg_pixel_count`* x *`avg_num_components`* x *`p_factor`*)

* *`avg_pixel_count`* すべての元のソース画像の平均ピクセルサイズ（幅 x 高さ）。 例えば、元の画像が通常 2k x 2k ピクセル前後の場合、これは 4M ピクセルになります。
* *`avg_num_components`* 画像の種類に応じて異なります。 ほとんどのRGB画像では 3 で、主に CMYK または RGBA 画像では 4 です。 画像の半分がRGBで、残りの半分が RGBA の場合は 3.5 を使用します。
* *`p_factor`* 画像が IC で変換される際の圧縮タイプと画質の設定に依存します。

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF 圧縮</b> </th> 
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
   <td> <p> 25～0.75（画像に応じる） </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG圧縮 </p> </td> 
   <td> <p> 1 ( 典型的なJPEGクォリティ 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>この近似は、ファイルシステムのオーバーヘッドを考慮しません。 ディスク上の実際の容量は、大幅に大きくなる場合があります。

**例**

画像サービングのデプロイメントでは、30,000 個の低解像度のレガシー画像を使用し、平均サイズは 500 x 500RGBピクセルである必要があります。 新しい印刷品質の画像データは、年間 10,000 件の割合で追加される予定です。 一般的な CMYK 画像サイズは 4k x 6k バイトです。 すべてのデータはJPEG圧縮され、高品質です。 3 年間の使用後のディスク容量の合計は、次のように推定されます。

*`total_space`* = 30,000 x (2k + 0.5k x 0.5k x 3 x 0.1) + 3 x 10,000 x (2k + 4k x 4 x 0.1) = 2.2 G + 268 GB =約 270 GB

最良の品質を保証するために、deflate(zip) 圧縮を使用できます。 仮定して *`p_factor`* 0.4 の場合、必要なディスク容量の合計は約 4 倍になります。 この場合、1 TB をわずかに超えます。
