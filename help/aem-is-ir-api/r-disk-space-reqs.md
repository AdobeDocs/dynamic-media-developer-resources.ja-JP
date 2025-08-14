---
title: ディスク容量の要件と推奨事項
description: ソフトウェアのインストールに必要なディスク容量の他に、イメージ・サービングには次のディスク容量の要件があります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---

# ディスク容量の要件と推奨事項{#disk-space-requirements-and-recommendations}

ソフトウェアのインストールに必要な容量に加えて、イメージ・サービングには次のディスク容量の要件があります。

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> 説明/ デフォルトの場所/次を使用して設定 </b> </th> 
   <th class="entry"> <b> 算定・提言 </b> </th> 
   <th class="entry"> <b> コメント </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Source画像、フォント、ICC プロファイル </b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>様々です。以下のコメントを参照してください。 </p> </td> 
   <td> <p>Image Server にのみアクセスできる必要があります。サーバーはデータを変更しません。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>HTTP 応答のデータキャッシュ </b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2、2 GB 以上を推奨します。 </p> </td> 
   <td> <p>このキャッシュには、ネストされた埋め込みデータと外部ソース画像も格納されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b> 画像カタログのデータキャッシュ </b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>カタログ フォルダがスペースの 1.5 倍を使用できるようにします。 </p> </td> 
   <td> <p>カタログが最初に読み込まれたときに生成されます。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b> ログデータ </b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>100 MB 以上。 </p> </td> 
   <td> <p>ログの設定とサーバーの使用に応じて異なります。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Image Server 一時ファイル </b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>ほとんどの場合は 100 MB で十分です。 </p> </td> 
   <td> <p>短時間のみ有効なデータです。PTIFF および特定の応答画像形式以外のソース画像に必要な場合があります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## ソースイメージのディスク容量要件 {#section-317da75099ad480d9a461c7e706d4f1c}

Adobeでは、画像コンバーターコマンドラインツール（IC）を使用して、すべてのソース画像を Pyramid TIFF ファイル形式（PTIFF）に変換することをお勧めします。 この変換により、すべてのアプリケーションに対して画像サービングの最適なランタイムパフォーマンスが確保されます。 Image Server は、IC で受け入れられるすべてのソースファイル形式を処理できますが、Dynamic Media はそのような使用をサポートしていません。

PTIFF ファイルを使用する場合は、次の経験則に従って、容量要件を判断できます。

*`total_space`* （バイト） = *`number_of_images`* × （2000 + *`avg_pixel_count`* x *`avg_num_components`* × *`p_factor`*）

* *`avg_pixel_count`* すべてのオリジナルのソース画像の平均ピクセルサイズ（幅 x 高さ）。 例えば、元の画像が通常 2k × 2k ピクセル程度の場合、4 メガピクセルになります。
* *`avg_num_components`* 画像のタイプによって異なります。 ほとんどのRGB画像の場合は 3 です。ほとんどの CMYK または RGBA 画像の場合は 4 です。 画像の半分がRGBで、残りの半分が RGBA の場合は、3.5 を使用します。
* *`p_factor`* 画像を IC で変換する際の圧縮の種類や設定する画質によって変わります。

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>PTIFF 圧縮 </b> </th> 
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
   <td> <p> 画像に応じて 25-0.75 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>JPEG圧縮 </p> </td> 
   <td> <p> 1 （JPEG quality 95 の場合は標準） </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>この概算では、ファイルシステムのオーバーヘッドは考慮されません。 ディスク上の実際のスペースは実質的に大きくてもよい。

**例**

画像サービングデプロイメントでは、30,000 個の低解像度のレガシー画像（平均サイズは 500 × 500 RGB ピクセル）を使用することが想定されています。 新しい印刷品質の画像データは、年間 10,000 の割合で追加されます。 一般的な CMYK 画像のサイズは 4k × 6k バイトです。 すべてのデータはJPEGで高品質に圧縮されます。 3 年間使用した後のディスク容量の合計は、次のように見積もられます。

*`total_space`* = 30,000 × （2k + 0.5k × 0.5k × 3 × 0.1） + 3 × 10,000 × （2k + 4k × 6k × 4 × 0.1） = 2.2 G + 268 GB =約 270 GB

最高の品質を保証するには、zip などの圧縮を使用できます。 0.4 の *`p_factor`* を仮定すると、必要なディスク容量は約 4 倍になります。 この場合、1 テラバイトを少し超えます。
