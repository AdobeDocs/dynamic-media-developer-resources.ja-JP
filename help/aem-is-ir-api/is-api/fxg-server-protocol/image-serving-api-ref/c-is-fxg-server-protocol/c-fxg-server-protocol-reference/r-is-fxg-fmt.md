---
description: 応答画像の形式：
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
TQID: 'https://experienceleague.adobe.com/tqpsn2LTwuUX-SDJTtMKhfpF391ZjjxohgfJn4a-Mdo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 307
ht-degree: 3%

---

# fmt{#fmt}

応答画像の形式：

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">形式</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> クライアントに送信される画像データの画像エンコーディング形式と、HTTP応答ヘッダーの対応する応答MIME タイプを指定します。 </p> <p> <span class="codeph"> jpeg </span>：非可逆JPEG </p> <p> <span class="codeph"> png </span>：損失のないPNG </p> <p> <span class="codeph"> png-alpha </span>: アルファチャンネル付きのロスレス PNG </p> <p> <span class="codeph"> tif </span>: TIFF </p> <p> <span class="codeph"> tif-alpha </span>: アルファチャンネル付きTIFF </p> <p> <span class="codeph"> swf </span>：非可逆JPEGをAdobe swf ファイルに埋め込む </p> <p> <span class="codeph"> pdf </span>:PDFに埋め込まれた画像 </p> <p> <span class="codeph"> gif </span>: 2 ～ 256色のGIF </p> <p> <span class="codeph"> gif-alpha </span>: 2～255色とキーカラーの透明度を備えたGIF </p> <p> <span class="codeph"> fxg </span>：変数とDOM操作が適用されたFXG </p> <p> <span class="codeph"> fxgraw </span>：元のFXGがサーバーに保存されています </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | グレー| cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 出力カラースペースのエフェクトに使用できます。 </p> <p> <span class="codeph"> rgb </span>: RGB image dataを返します </p> <p> <span class="codeph"> グレー</span>: グレースケール画像データを返します </p> <p> <span class="codeph"> cmyk </span>: CMYK画像データを返します </p> </td> 
 </tr> 
</table>

`tiffCompression`は、tif、tif-alphaが形式として指定されている場合にのみ許可されます。 これらの画像形式でサポートされる圧縮オプションについては、次の表を参照してください。

`qlt=`を使用して、JPEGとJPEGの圧縮を含むTIFFの形式のJPEG エンコーディングオプションを設定できます。 quantize=は、fmt=gifまたはfmt=gif-alphaの場合に使用できます。 詳しくは、コマンドの説明を参照してください。 他の形式には設定可能なオプションはありません。

すべての形式と`pixelTypes[7]`に対して、ピクセルコンポーネントあたり8 ビットが返されます。

次の表に、形式と`pixelType`の有効な組み合わせ（対応するHTTP応答MIME タイプ）を示します。

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname">形式</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>応答のMIME タイプ </p> </th> 
   <th colname="col4" class="entry"> <p>ICC プロファイルを埋め込む </p> </th> 
   <th colname="col5" class="entry"> <p>オプション </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb、グレー、cmyk </p> </td> 
   <td> <p>&lt;image/jpeg&gt; </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png, png-alpha </p> </td> 
   <td> <p>rgb、グレー </p> </td> 
   <td> <p>&lt;image/png&gt; </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif, tif-alpha </p> </td> 
   <td> <p>rgb、グレー、cmyk </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> （none | lzw | zip | jpeg）, qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf, swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application/x-shockwave-flash&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> qlt= </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>PDF </p> </td> 
   <td> <p>rgb、グレー、cmyk </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif-alpha </p> </td> 
   <td> <p>rgb、グレー </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> quantize=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
