---
title: ディスク領域の要件と推奨事項
description: ソフトウェアのインストールに必要な領域の他に、Image Servingには次のディスク領域の要件があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
TQID: 'https://experienceleague.adobe.com/F-ZFmPc2IDzE4ztCqZ9xstW1b5yBGkzBDjv4IRa5OCQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 514
ht-degree: 0%

---

# ディスク領域の要件と推奨事項{#disk-space-requirements-and-recommendations}

ソフトウェアのインストールに必要な容量のほかに、Image Servingには次のディスク容量の要件があります。

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>説明/ デフォルトの場所/ </b>で設定 </th> 
   <th class="entry"> <b>計算/推奨事項</b> </th> 
   <th class="entry"> <b> コメント </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Sourceの画像、フォント、ICC プロファイル </b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph">は：:RootPaths </span>です </p> </td> 
   <td> <p>様々です。以下のコメントを参照してください。 </p> </td> 
   <td> <p>Image Serverのみがアクセスできる必要があります。サーバーはデータを変更しません。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP応答データキャッシュ </b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2、少なくとも2 GBを推奨 </p> </td> 
   <td> <p>このキャッシュには、ネスト/埋め込みデータと外部ソース画像も保存されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>画像カタログデータキャッシュ </b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>カタログフォルダーでスペースの1.5倍を使用できるようにします。 </p> </td> 
   <td> <p>カタログが最初に読み込まれたときに入力されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b> ログデータ </b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph">は：:LogFile </span>です </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100MB以上。 </p> </td> 
   <td> <p>これは、ログの設定とサーバーの使用によって異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Image Serverの一時ファイル </b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph">は：:TempDirectory </span>です </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 MBで十分です。 </p> </td> 
   <td> <p>短期的なデータ。PTIFFと特定の応答画像フォーマット以外のソース画像に必要な場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ソース・イメージのディスク領域の要件 {#section-317da75099ad480d9a461c7e706d4f1c}

Adobeでは、Image Converter コマンドラインツール（IC）を使用して、すべてのソース画像をピラミッド TIFF ファイル形式（PTIFF）に変換することをお勧めします。 この変換により、すべてのアプリケーションに対して画像サービングの最適なランタイムパフォーマンスが確保されます。 Image Serverは、ICが受け入れたすべてのソースファイル形式を処理できますが、Dynamic Mediaはそのような使用をサポートしていません。

PTIFF ファイルを使用する場合は、次の経験則を使用すると、スペース要件を判断できます。

*`total_space`* （バイト） = *`number_of_images`* × （2000 + *`avg_pixel_count`* x *`avg_num_components`* × *`p_factor`*）

* *`avg_pixel_count`*&#x200B;すべての元のソース画像の平均ピクセルサイズ（幅x高さ）。 例えば、元の画像が通常2,000 ピクセル×2,000 ピクセル程度である場合、これは4 メガピクセルになります。
* *`avg_num_components`*&#x200B;画像の種類によって異なります。 RGB画像の場合は3で、CMYK画像やRGBA画像の場合は4です。 画像の半分がRGBで、残りの半分がRGBAの場合は3.5を使用します。
* *`p_factor`*&#x200B;画像がICで変換されるときの圧縮タイプと画質セットによって異なります。

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
   <td> <p>デフレート圧縮 </p> </td> 
   <td> <p> 画像に応じて、25 ～ 0.75 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG Compression </p> </td> 
   <td> <p> 1 （JPEGクォリティ 95で典型的） </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>この近似は、ファイルシステムのオーバーヘッドを考慮しません。 ディスク上の実際のスペースは、かなり大きくてもよい。

**例**

Image Service デプロイメントでは、30,000枚の低解像度レガシー画像を使用し、平均サイズは500 × 500 RGB ピクセルです。 新しい印刷品質の画像データが年間10,000の割合で追加されます。 CMYK画像の一般的なサイズは4k×6k バイトです。 すべてのデータはJPEGで高品質に圧縮されています。 3年間の使用後のディスク領域の合計量は、次のように見積もられます。

*`total_space`* = 30,000 × （2k + 0.5k × 0.5k × 3 × 0.1） + 3 × 10,000 × （2k + 4k × 6k × 4 × 0.1） = 2.2 G + 268 GB =約270 GB

保証された最もよい質のために、郵便番号のような圧縮は採用することができる。 *`p_factor`*&#x200B;が0.4の場合、必要なディスク領域の合計容量は約4倍大きくなります。 この場合は、1 テラバイト強です。
