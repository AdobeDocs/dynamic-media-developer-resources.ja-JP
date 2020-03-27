---
description: カラー値 色の値は、16進数表記、コンポーネント値のカンマ区切りリストまたは小数を使用して指定できます。
seo-description: カラー値 色の値は、16進数表記、コンポーネント値のカンマ区切りリストまたは小数を使用して指定できます。
seo-title: color
solution: Experience Manager
title: color
topic: Scene7 Image Serving - Image Rendering API
uuid: 61308b8e-eaac-4b2e-8500-2f9efa8a6ce8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# color{#color}

カラー値 色の値は、16進数表記、コンポーネント値のカンマ区切りリストまたは小数を使用して指定できます。

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 色</span></span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">{{<span class="varname"> gray</span>[,alpha<span class="varname"></span>][g]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> red red</span>green<span class="varname"> ,</span>blue<span class="varname"> [ ,</span>rgbAlpha<span class="varname"></span>r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> cyan</span>magenta <span class="varname"> ,</span>, black <span class="varname"> yellow</span>, <span class="varname"> black</span>magenta[alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|hex8<span class="varname"></span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|hex10<span class="varname"></span>}k}[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 赤</span>、緑 <span class="varname"> 、</span>青 <span class="varname"> 、</span><span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>colorコンポーネント値（0 ～ 255、10進整数） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> シ <span class="varname"> アン，マゼンタ</span>，イエロー <span class="varname"> ,</span>ブラック， <span class="varname"></span><span class="varname"></span><span class="varname"> アルファ</span></span> </p></td> 
  <td class="stentry"> <p>CMYKカラー成分値（0.100 %、10進数整数） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> グレ <span class="varname"> ー</span>、アルファ <span class="varname"> 値</span></span> </p> </td> 
  <td class="stentry"> <p>グレーの色成分の値（0...100%、10進整数） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>パック2桁の16進グレーカラー値(GG) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>アルファ値を持つ4桁のパック16進グレー(GGAA) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>パック6桁の16進数RGBカラー値(RRGGBB) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>8桁のパック16進数RGBA(RRGGBBAA)またはCMYK(CCMMYYKK)のカラー値（「k」サフィックスを付けて指定した場合） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>アルファ値を含む10桁のパック16進CMYK(CCYYMMKKAA) </p> </td> 
 </tr> 
</table>

RGBカラーの10進数値は、0 ～ 255の範囲です。 CMYKとグレーの小数成分の値は0 ～ 100%の範囲です。 すべての16進値は、0 ～ 0xFFの範囲です。

色成分の値は、アルファ値に依存しない値（事前乗算された値ではない）と見なされます。

すべての色の値、接頭辞、接尾辞では大文字と小文字が区別されません。

CMYKカラー値には、タイプサフィックス「k」が必要です。 タイプサフィックスは、RGBおよびグレーのカラー値に対してオプションで指定できます。

16進数のグレーカラー値には、プレフィックス「0x」が必要です。

「s」サフィックスは、色の値が、（で定義された）色の値のピクセルタイプに対応する入力（ソース）カラースペースに関連付けられることを指定し `attribute::IccProfileSrc*`ます。 このサフィックスが存在しない場合、カラー値は出力（出力先）のカラースペース（またはで定義）に関連付 `icc=` けられ `attribute::IccProfile*`ます。

## 初期設定 {#section-737082a7da544acca8092a48d88480e7}

アルファ値が明示的に指定されていない場合、255、0xFFまたは100%（完全に不透明）と見なされます。

## 例 {#section-4ac69026349949f8b595a6d4a9ce474d}

有効なカラー指定子の例、および対応するピクセルタイプ、カラー値、アルファ値、初期設定のカラースペースの例を次に示します。

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>色</i></b> </th> 
   <th class="entry"> <b>ピクセルタイプ</b> </th> 
   <th class="entry"> <b>カラー値</b> </th> 
   <th class="entry"> <b>アルファ値</b> </th> 
   <th class="entry"> <b>デフォルトのカラースペース </b> </th> 
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
   <td> <p>灰色 </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileSrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75g </p> </td> 
   <td> <p>灰色 </p> </td> 
   <td> <p>50% </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>灰色 </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> <span class="codeph"> IccProfileGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0xddeegs </p> </td> 
   <td> <p>灰色 </p> </td> 
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

で指定した出力カラースペースは、 `icc=` 出力カラーのピクセルタイプが出力画像のピクセルタイプに対応する場合、初期設定のカラースペースの代わりに適用されます。
