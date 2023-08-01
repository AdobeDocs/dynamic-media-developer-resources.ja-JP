---
description: カラー値。 色の値は、16 進数表記、コンポーネント値のコンマ区切りリストまたは小数を使用して指定できます。
solution: Experience Manager
title: color
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eba88ff0-877d-432e-bbd6-9172f5b460e9
source-git-commit: 2ff380ad30911a85bc066ae53f0cb69360ed99e4
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 13%

---

# color{#color}

カラー値。 色の値は、16 進数表記、コンポーネント値のコンマ区切りリストまたは小数を使用して指定できます。

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> カラー</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">&amp;lcub;&amp;lcub;<span class="varname"> グレー</span>[,<span class="varname"> アルファ</span>][g&amp;rcub;|</span> </p> <p> <span class="codeph"> {<span class="varname"> 赤</span>,<span class="varname"> 緑</span>,<span class="varname"> 青</span>[ ,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> シアン</span>, <span class="varname"> マゼンタ</span>, <span class="varname"> 黄色</span>, <span class="varname"> 黒</span>[,alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}&amp;rcub;[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 赤</span>, <span class="varname"> 緑</span>, <span class="varname"> 青</span>, <span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>色コンポーネント値（0...255、小数整数） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> シアン</span>, <span class="varname"> マゼンタ</span>, <span class="varname"> 黄色</span>, <span class="varname"> 黒</span>, <span class="varname"> アルファ</span></span> </p></td> 
  <td class="stentry"> <p>CMYK カラーコンポーネント値（0.100 %、小数点以下整数） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> グレー</span>, <span class="varname"> アルファ</span></span> </p> </td> 
  <td class="stentry"> <p>グレーカラーコンポーネントの値（0...100%、小数点以下整数） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>パック 2 桁の 16 進グレー値 (GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>アルファカラー値を持つ 4 桁のパック 16 進グレー (GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>パック 6 桁の 16 進数RGBカラー値 (RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>8 桁のパック 16 進数 RGBA(RRGGBBAA) または CMYK(CCMMYYKK) のカラー値（「k」サフィックスを付けて指定する場合） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>アルファ値を持つ 10 桁のパック 16 進 CMYK (CCYYMMKKAA) </p> </td> 
 </tr> 
</table>

RGBの色の 10 進数のコンポーネント値は、0 ～ 255 の範囲です。 CMYK およびグレーの 10 進数コンポーネントの値は、0 ～ 100%の範囲です。 16 進数のコンポーネント値は、すべて 0 ～ 0 xFF の範囲です。

カラーコンポーネントの値は、アルファ値とは無関係（プリマルチプライではない）と見なされます。

すべての色の値、プレフィックス、サフィックスは、大文字と小文字が区別されません。

CMYK カラー値には、タイプサフィックス「k」が必要です。 必要に応じて、RGBとグレーのカラー値にタイプサフィックスを指定できます。

16 進数のグレーカラー値には、プレフィックス「0x」が必要です。

「s」サフィックスは、色の値が、色の値 ( `attribute::IccProfileSrc*`) をクリックします。 このサフィックスが存在しない場合、色の値は出力（宛先）の色空間に関連付けられます ( `icc=` または `attribute::IccProfile*`) をクリックします。

## 初期設定 {#section-737082a7da544acca8092a48d88480e7}

アルファ値が明示的に指定されていない場合は、255、0xFF、100%（完全な不透明）と見なされます。

## 例 {#section-4ac69026349949f8b595a6d4a9ce474d}

有効なカラー指定子、および対応するピクセルタイプ、カラー値、アルファ値、デフォルトカラースペースの例を以下に示します。

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>カラー</i> </b> </th> 
   <th class="entry"> <b>ピクセルタイプ</b> </th> 
   <th class="entry"> <b>カラー値</b> </th> 
   <th class="entry"> <b>アルファ値</b> </th> 
   <th class="entry"> <b>初期設定のカラースペース </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0,100,200,200rs </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>200 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x010203S </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>1,2,3 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>a0b1c2d3R </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>160,177,194 </p> </td> 
   <td> <p>211 </p> </td> 
   <td> <p> <span class="codeph"> IccProfileRgb</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100S </p> </td> 
   <td> <p>グレー </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75g </p> </td> 
   <td> <p>グレー </p> </td> 
   <td> <p>50% </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>グレー </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>グレー </p> </td> 
   <td> <p>87% </p> </td> 
   <td> <p>93% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>94,11,50,33k </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>94-11-50-33% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26KS </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22-23-24-25% </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56-57-58-59% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileCmyk</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcCmyk</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

で指定された出力カラースペース `icc=` 出力カラーのピクセルタイプが出力画像のピクセルタイプに対応している場合に、デフォルトのカラースペースの代わりに適用されます。
