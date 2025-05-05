---
description: カラー値。 カラー値は、16 進表記、コンポーネント値のコンマ区切りリスト、または小数を使用して指定できます。
solution: Experience Manager
title: color
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eba88ff0-877d-432e-bbd6-9172f5b460e9
source-git-commit: 2ff380ad30911a85bc066ae53f0cb69360ed99e4
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 3%

---

# color{#color}

カラー値。 カラー値は、16 進表記、コンポーネント値のコンマ区切りリスト、または小数を使用して指定できます。

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> color</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">&lcub;&lcub;<span class="varname"> gray</span>[,<span class="varname"> alpha</span>][g]&rcub;|</span> </p> <p> <span class="codeph"> {<span class="varname"> red</span>,<span class="varname"> green</span>,<span class="varname"> blue</span>[ ,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> cyan</span>, <span class="varname"> magenta</span>, <span class="varname"> yellow</span>, <span class="varname"> black</span>[,alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}&rcub;[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> red</span>、<span class="varname"> green</span>、<span class="varname"> blue</span>、<span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>色コンポーネント値（0...255、小数点） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cyan</span>、<span class="varname"> magenta</span>、<span class="varname"> yellow</span>、<span class="varname"> black</span>、<span class="varname"> alpha</span></span> </p></td> 
  <td class="stentry"> <p>CMYK カラーコンポーネント値（0..100 %、10 進数の整数） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> グレー </span>、<span class="varname"> アルファ </span></span> </p> </td> 
  <td class="stentry"> <p>グレーカラーコンポーネント値（0...100%、小数点） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>パックされた 2 桁の 16 進数のグレーカラー値（GG） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>アルファ カラー値を持つ 4 桁の 16 進数グレー（GGA） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>パックされた 6 桁の 16 進RGBカラー値（RRGGBB） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>パックされた 8 桁の 16 進数 RGBA （RRGGBAA）または CMYK （CCMMYYKK）カラー値（「k」サフィックスで指定された場合） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex10</span> </span> </p></td> 
  <td class="stentry"> <p>アルファ値を持つ 10 桁の 16 進数 CMYK のパック （CCYYMKKAA） </p> </td> 
 </tr> 
</table>

RGBカラーの小数部の値は、0 ～ 255 の範囲です。 CMYK およびグレーの小数点以下のコンポーネント値は、0 ～ 100% の範囲です。 すべての 16 進数コンポーネント値の範囲は 0...0xFF です。

カラーコンポーネントの値は、アルファ値とは無関係であると見なされます（乗算前ではありません）。

すべてのカラー値、接頭辞、接尾辞では、大文字と小文字が区別されません。

CMYK カラー値には、タイプのサフィックス「k」が必要です。 オプションで、RGBカラー値とグレーカラー値に対して型サフィックスを指定できます。

16 進数のグレー値には、プレフィックス &#39;0x&#39;が必要です。

&#39;s&#39; サフィックスは、カラー値が、カラー値のピクセルタイプ （`attribute::IccProfileSrc*` で定義）に対応する入力（ソース） カラースペースに関連付けられることを指定します。 このサフィックスが存在しない場合、カラー値は出力（出力先）カラースペース（`icc=` または `attribute::IccProfile*` で定義）に関連付けられます。

## 初期設定 {#section-737082a7da544acca8092a48d88480e7}

アルファ値が明示的に指定されていない場合は、255、0xFF、または 100% （完全に不透明）であると見なされます。

## 例 {#section-4ac69026349949f8b595a6d4a9ce474d}

有効なカラー指定子と、それに対応するピクセルタイプ、カラー値、アルファ値、デフォルトカラースペースの例を次に示します。

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i> 色 </i> </b> </th> 
   <th class="entry"> <b> ピクセルタイプ </b> </th> 
   <th class="entry"> <b> カラー値 </b> </th> 
   <th class="entry"> <b>Alpha値 </b> </th> 
   <th class="entry"> <b> デフォルトのカラースペース </b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>RGB </p> </td> 
   <td> <p>0,100,200 </p> </td> 
   <td> <p>255 </p> </td> 
   <td> <p> IccProfileRgb を <span class="codeph"> す </span> </p> </td> 
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
   <td> <p> IccProfileRgb を <span class="codeph"> す </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>100S </p> </td> 
   <td> <p>グレー </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> <span class="codeph"> SrcGray</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>50,75g </p> </td> 
   <td> <p>グレー </p> </td> 
   <td> <p>50% </p> </td> 
   <td> <p>75% </p> </td> 
   <td> <p> IccProfileGray<span class="codeph"> 指定 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0X70G </p> </td> 
   <td> <p>グレー </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p>44% </p> </td> 
   <td> <p> IccProfileGray<span class="codeph"> 指定 </span> </p> </td> 
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
   <td> <p> IccProfileCmyk を <span class="codeph"> す </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>22,23,24,25,26KS </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>22-23-24-25% </p> </td> 
   <td> <p>26% </p> </td> 
   <td> <p> IccProfileSrcCmyk を <span class="codeph"> 定 </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>38393A3bK </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>56-57-58-59% </p> </td> 
   <td> <p>100% </p> </td> 
   <td> <p> IccProfileCmyk を <span class="codeph"> す </span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p>0x0a0b0C0d0eks </p> </td> 
   <td> <p>CMYK </p> </td> 
   <td> <p>10-11-12-13% </p> </td> 
   <td> <p>14% </p> </td> 
   <td> <p> IccProfileSrcCmyk を <span class="codeph"> 定 </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

出力色のピクセルタイプが出力画像のピクセルタイプに対応する場合、`icc=` で指定された出力色空間がデフォルトの色空間の代わりに適用されます。
