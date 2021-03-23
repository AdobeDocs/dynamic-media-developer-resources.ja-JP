---
description: 応答画像の形式。
seo-description: 応答画像の形式。
seo-title: fmt
solution: Experience Manager
title: fmt
uuid: 78ee7545-5ad9-4240-bbfc-20efe3e42ed3
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 3%

---


# fmt{#fmt}

応答画像の形式。

`fmt=format [,pixelType ]`

<table id="simpletable_66FAABB7BD7A4BBB815A570BEA4C1AE8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 形式</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> jpeg | png | png-alpha | tif | tif-alpha | swf | pdf | gif | gif-alpha | fxg | fxgraw</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> クライアントに送信する画像データの画像エンコーディング形式と、HTTP応答ヘッダーの対応する応答MIMEタイプを指定します。 </p> <p> <span class="codeph">  jpeg  </span>:非可逆圧縮JPEG </p> <p> <span class="codeph"> png  </span>:可逆圧縮PNG </p> <p> <span class="codeph"> png-alpha  </span>:アルファチャネル付き可逆圧縮PNG </p> <p> <span class="codeph">  tif  </span>:TIFF </p> <p> <span class="codeph"> tif-alpha  </span>:アルファチャネルのTIFF </p> <p> <span class="codeph">  swf  </span>:Adobeswfファイルに埋め込まれた非可逆圧縮JPEG </p> <p> <span class="codeph"> pdf  </span>:PDFに埋め込まれた画像 </p> <p> <span class="codeph"> gif  </span>:2 ～ 256色のGIF </p> <p> <span class="codeph"> gif-alpha  </span>:キーカラーの透明部分がプラスされた2 ～ 255色のGIF </p> <p> <span class="codeph"> fxg  </span>:変数とDOM操作が適用されたFXG </p> <p> <span class="codeph">  fxgraw  </span>:元のFXGをサーバに保存 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> pixelType</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> rgb | gray | cmyk</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"></td> 
  <td class="stentry"> <p> 出力カラースペースの効果に使用できます。 </p> <p> <span class="codeph">  rgb  </span>:rgb画像データを返す </p> <p> <span class="codeph"> グレ </span>ー：グレースケール画像データを返す </p> <p> <span class="codeph"> cmyk  </span>:CMYK画像データを返す </p> </td> 
 </tr> 
</table>

`tiffCompression` は、tif、tif-alphaが形式として指定されている場合にのみ使用できます。これらの画像形式でサポートされる圧縮オプションについては、次の表を参照してください。

`qlt=` を使用して、次の形式のJPEGエンコーディングオプションを設定できます。JPEG、JPEG圧縮時のTIFF。quantize=は、fmt=gifまたはfmt=gif-alphaの場合に使用できます。 詳細については、コマンドの説明を参照してください。 その他の形式では、設定可能なオプションはありません。

すべての形式と`pixelTypes[7]`に対して、ピクセルあたり8ビットのコンポーネントが返されます。

次の表に、有効な形式と`pixelType`の組み合わせ（対応するHTTP応答のMIMEタイプ）を示します。

<table id="table_54AFE58185004C74971EFBA845E177B6"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p><span class="varname"> フォーマット</span> </p> </th> 
   <th colname="col2" class="entry"> <p><span class="varname"> pixelType</span> </p> </th> 
   <th colname="col3" class="entry"> <p>応答のMIMEタイプ </p> </th> 
   <th colname="col4" class="entry"> <p>ICCプロファイルを埋め込む </p> </th> 
   <th colname="col5" class="entry"> <p>オプション </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>jpeg </p> </td> 
   <td> <p>rgb、グレー、cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>png、png-alpha </p> </td> 
   <td> <p>rgb、グレー </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>tif、tif-alpha </p> </td> 
   <td> <p>rgb、グレー、cmyk </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p><span class="codeph"> <span class="varname"> tiffCompression</span> ( none | lzw | zip | jpeg)、qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>swf、swf-alpha </p> </td> 
   <td> <p>rgb </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> qlt=  </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>PDF </p> </td> 
   <td> <p>rgb、グレー、cmyk </p> </td> 
   <td> <p>&lt;application&gt; </p> </td> 
   <td> <p>はい </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>gif、gif-alpha </p> </td> 
   <td> <p>rgb、グレー </p> </td> 
   <td> <p>&lt;image&gt; </p> </td> 
   <td> <p>no </p> </td> 
   <td> <p><span class="codeph"> 量子化=</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 例 {#section-2135175ab3ec453f9f5388d5690b0da4}

[!DNL http://server/is/agm/myRootId/myImageId?fmt=swf]
