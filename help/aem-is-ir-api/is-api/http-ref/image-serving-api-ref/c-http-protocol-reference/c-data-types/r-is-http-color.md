---
description: カラー値。 カラー値は、16進数表記、コンマ区切りのコンポーネント値リスト、または10進数を使用して指定できます。
solution: Experience Manager
title: color
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eba88ff0-877d-432e-bbd6-9172f5b460e9
TQID: 'https://experienceleague.adobe.com/3NfMrvwXTP9A-KoxjVPtps-0rhO5xNd04WUlrdCQEo8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 456
ht-degree: 9%

---

# color{#color}

カラー値。 カラー値は、16進数表記、コンマ区切りのコンポーネント値リスト、または10進数を使用して指定できます。

<table id="simpletable_9EBE66066E854ABE978F8F7ADC66BDE3"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> カラー</span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph">&lcub;&lcub;<span class="varname"> grey</span>[,<span class="varname"> alpha</span>][g]&rcub;|</span> </p> <p> <span class="codeph"> {<span class="varname"> red</span>,<span class="varname"> green</span>,<span class="varname"> blue</span>[ , ,<span class="varname"> rgbAlpha</span>][r]}|</span> </p> <p> <span class="codeph"> {<span class="varname"> cyan</span>, <span class="varname"> magenta</span>, <span class="varname"> yellow</span>, <span class="varname"> black</span>[,alpha]k}|</span> </p> <p> <span class="codeph"> {0x{hex2|hex4}[g]}|</span> </p> <p> <span class="codeph">{[0x]{<span class="varname"> hex6</span>|<span class="varname"> hex8</span>}[r]}|</span> </p> <p> <span class="codeph"> {[0x]{<span class="varname"> hex8</span>|<span class="varname"> hex10</span>}k}&rcub;[s]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> red</span>、<span class="varname"> green</span>、<span class="varname"> blue</span>、<span class="varname"> rgbAlpha</span></span> </p> </td> 
  <td class="stentry"> <p>カラーコンポーネントの値（0...255、10進数int） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> シアン </span>、<span class="varname"> マゼンタ </span>、<span class="varname"> イエロー</span>、<span class="varname"> ブラック </span>、<span class="varname"> アルファ </span></span> </p></td> 
  <td class="stentry"> <p>CMYK カラーコンポーネントの値（0..100 %、小数点以下桁） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> グレー</span>、<span class="varname"> アルファ </span></span> </p> </td> 
  <td class="stentry"> <p>グレーのカラーのコンポーネント値（0...100%、小数点以下の整数） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex2</span> </span> </p></td> 
  <td class="stentry"> <p>パッケージ化された2桁の16進グレーのカラー値（GG） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex4</span> </span> </p> </td> 
  <td class="stentry"> <p>アルファカラー値（GGAA）を含む4桁の16進数グレー </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex6</span> </span> </p> </td> 
  <td class="stentry"> <p>6桁の16進数RGB カラー値（RRGGBB） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> hex8</span> </span> </p> </td> 
  <td class="stentry"> <p>パッケージ化された8桁の16進数RGBA （RRGGBBAA）またはCMYK （CCMMYYKK）カラー値（「k」接尾辞で指定されている場合） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 16月10日</span> </span> </p></td> 
  <td class="stentry"> <p>アルファ値（CCYYMMKKAA）を持つ10桁の16進数CMYKのパック </p> </td> 
 </tr> 
</table>

RGB カラーの10進数のコンポーネント値は、0 ～ 255の範囲です。 CMYKとグレーの10進数成分の値は0..100%の範囲です。 すべての16進数コンポーネント値は、0...0xFFの範囲です。

カラーコンポーネントの値は、アルファ値とは独立していると見なされます（事前に乗算されるわけではありません）。

すべてのカラー値、接頭辞、接尾辞では、大文字と小文字は区別されません。

CMYK カラー値には、接尾辞「k」が必要です。 RGBとグレーのカラー値には、オプションで文字サフィックスを指定できます。

16進数のグレーのカラー値には、接頭辞「0x」が必要です。

&#39;s&#39;接尾辞は、カラー値が、カラー値（`attribute::IccProfileSrc*`で定義）のピクセルタイプに対応する入力（ソース）カラースペースに関連付けられていることを指定します。 この接尾辞が存在しない場合、カラー値は出力（出力先）カラースペース（`icc=`または`attribute::IccProfile*`で定義）に関連付けられます。

## 初期設定 {#section-737082a7da544acca8092a48d88480e7}

アルファ値が明示的に指定されていない場合は、255、0xFF、または100% （完全に不透明）と見なされます。

## 例 {#section-4ac69026349949f8b595a6d4a9ce474d}

有効なカラー指定子の例と、対応するピクセルタイプ、カラー値、アルファ値、デフォルトのカラースペースの例を以下に示します。

<table id="table_1539E74A1EC545F1B5398D86A27079D1"> 
 <thead> 
  <tr> 
   <th class="entry"> <b> <i>色</i> </b> </th> 
   <th class="entry"> <b> ピクセルタイプ </b> </th> 
   <th class="entry"> <b> カラー値</b> </th> 
   <th class="entry"> <b>Alpha値</b> </th> 
   <th class="entry"> <b>既定のカラースペース </b> </th> 
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
   <td> <p>100秒 </p> </td> 
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

出力カラーのピクセルタイプが出力画像のピクセルタイプに対応する場合、デフォルトのカラースペースの代わりに`icc=`で指定された出力カラースペースが適用されます。
