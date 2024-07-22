---
description: 応答画像の形式。
solution: Experience Manager
title: fmt
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e179fc51-0461-4000-99eb-4390c35d5606
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 3%

---

# fmt{#fmt}

応答画像の形式。

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 形式 </span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif アルファ | swf | pdf | gif | gif アルファ | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> クライアントに送信する画像データの画像エンコーディング形式と、HTTP 応答ヘッダーに対応する応答 MIME タイプを指定します。 </p> <p> <span class="codeph"> jpeg </span>：非可逆JPEG </p> <p> <span class="codeph"> png </span>：損失のない PNG </p> <p> <span class="codeph"> png-alpha </span>：アルファチャネルを使用した損失のない PNG </p> <p> <span class="codeph"> tif </span>:TIFF </p> <p> <span class="codeph"> tif-alpha </span>：アルファチャンネルを持つTIFF </p> <p> <span class="codeph"> swf </span>:Adobe swf ファイルに埋め込まれた非可逆JPEG </p> <p> <span class="codeph"> pdf </span>:PDFに埋め込まれた画像 </p> <p> <span class="codeph"> gif </span>:2～256 色のGIF </p> <p> <span class="codeph"> gif-alpha </span>:2～255 色とキーカラーの透明度を備えたGIF </p> <p> <span class="codeph"> fxg </span>：変数と DOM 操作が適用された FXG </p> <p> <span class="codeph"> fxgraw </span>: サーバーに保存された元の FXG </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb |灰色 | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 出力カラースペースに影響を与えるために使用できます。 </p> <p> <span class="codeph"> rgb </span>:RGB画像データを返します </p> <p> <span class="codeph"> gray </span>：グレースケールの画像データを返します </p> <p> <span class="codeph"> cmyk </span>:CMYK 画像データを返します </p> </td> 
 </tr> 
</table>

`tiffCompression` は、tif、tif-alpha が形式として指定されている場合にのみ使用できます。 これらの画像形式でサポートされる圧縮オプションについては、次の表を参照してください。

JPEG、JPEG圧縮 `qlt=` 使用したTIFFなど、JPEGエンコーディングオプションを設定できます。 quantize=は、fmt=gif または fmt=gif-alpha の場合に使用できます。 詳細は、コマンドの説明を参照してください。 その他の形式には、設定可能なオプションはありません。

8 ビット/ピクセルのコンポーネントは、すべての形式および `pixelTypes[7]` に対して返されます。

次の表に、形式と `pixelType` の有効な組み合わせ、対応する HTTP 応答の MIME タイプを示します。

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> 形式 </span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>応答の MIME タイプ </p> </th> 
   <th colname="col4" class="entry"> <p>ICC プロファイルを埋め込む </p> </th> 
   <th colname="col5" class="entry"> <p>オプション </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb, グレー，cmyk </p> </td> 
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
   <td> <p>tif、tif-alpha </p> </td> 
   <td> <p>rgb, グレー，cmyk </p> </td> 
   <td> <p>&lt;image/tiff&gt; </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> （なし） | lzw |郵便番号 | jpeg）, qlt=</span> </p> </td> 
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
   <td> <p>rgb, グレー，cmyk </p> </td> 
   <td> <p>&lt;application/pdf&gt; </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif, gif アルファ </p> </td> 
   <td> <p>rgb、グレー </p> </td> 
   <td> <p>&lt;image/gif&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> quantize=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
