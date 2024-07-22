---
title: 発作
description: 応答画像適合モード。 スケール係数の計算方法を指定します。この係数は、応答サイズが wid=および hei=で指定され、scl=が存在しない場合に、合成画像を応答画像にスケールするために使用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '490'
ht-degree: 1%

---

# 発作{#fit}

応答画像適合モード。 スケール係数の計算方法を指定します。この係数は、応答サイズが wid=および hei=で指定され、scl=が存在しない場合に、合成画像を応答画像にスケールするために使用されます。

` fit= *`mode`*, *`upscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mode </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> フィット|拘束|切り抜き|折り返し|ストレッチ|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> アップスケール </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

次のモードオプションの説明では、*`xScale`* は合成画像の幅と応答画像の幅の比率、*`yScale`* は合成画像の高さと応答画像の高さの比率であると想定しています。

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> パラメータ </th> 
   <th colname="col2" class="entry"> 定義 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> fit </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> wid= </span> および <span class="codeph"> hei= </span> で割り当てられたスペースに収まるように合成画像を拡大/縮小します。スペースは最小限で、切り抜きは行われません。 応答画像は、wid= </span> および <span class="codeph"> hei= </span><span class="codeph"> 指定された正確なサイズです。 xScale </span> と yScale </span><span class="varname"> 中で小さい方 <span class="varname"> 適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> constraint </span> </p> </td> 
   <td colname="col2"> <p>合成画像を <span class="codeph"> fit </span> のように拡大縮小して、<span class="codeph"> wid= </span> および <span class="codeph"> hei= </span> で割り当てられたスペースに収まるようにします。ただし、実際の応答画像は、空白を避けるために、<span class="codeph"> wid= </span> および <span class="codeph"> hei= </span> で指定されたサイズよりも小さい場合があります。 xScale </span> と yScale </span><span class="varname"> 中で小さい方 <span class="varname"> 適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> crop </span> </p> </td> 
   <td colname="col2"> <p>合成画像のサイズを調整して、応答画像全体に表示します。切り抜きは最小限に抑えられ、空白文字は入りません。 xScale </span> と yScale </span><span class="varname"> 大きい方 <span class="varname"> 適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> wrap </span> </p> </td> 
   <td colname="col2"> <p>切り抜き </span> と同様 <span class="codeph"> 合成画像を拡大縮小して、応答画像全体を覆いますが、実際の応答画像は、切り抜きを避けるために <span class="codeph"> wid= </span> および <span class="codeph"> hei= </span> で指定されるよりも大きくなる場合があります。 xScale </span> と yScale </span><span class="varname"> 大きい方 <span class="varname"> 適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> stretch </span> </p> </td> 
   <td colname="col2"> <p>合成画像を x と y で個別に拡大縮小し、切り抜きや空白の挿入を行わずに、応答画像全体を埋めます。 これにより、通常、画像の縦横比が変更されます。 <span class="varname"> xScale </span> は水平スケーリングに、yScale </span> は垂直スケーリングに使用 <span class="varname"> れます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hfit </span> </p> </td> 
   <td colname="col2"> <p>xScale </span><span class="varname"> 適用して、画像を水平方向にしっかりと収め、上部や下部に切り抜きや空白を配置します。 特殊な用途に便利です。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>yScale </span><span class="varname"> 適用して、画像を垂直方向にしっかりとフィットさせます。場合によっては、左や右に切り抜きや空白が表示されます。 特殊な用途に便利です。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`upscale`* を「1」に設定するとアップスケールが許可され、「0」に設定すると*`xScale`*が制限され、「*`yScale`*」は 1:1 に制限されます。 アップスケールが無効な場合、合成画像が応答画像よりも小さい場合、追加の空白が存在する可能性があります。

デフォルトでは、切り抜きと空白は中央に配置されます。それらの位置は `align=` で制御できます。 ホワイトスペースの塗りつぶしの色と不透明度は、`bgc=` によって決まります。

## プロパティ {#section-6d7a5a7e18434bca9bc2fdb236af8909}

ビュー属性。 現在のレイヤ設定に関係なく適用されます。 `wid=` または `hei=` の少なくとも 1 つを指定する必要があります。指定しないと、エラーが返されます。説明に従ってはめあいモードが動作するには、`wid=` と `hei=` の両方を指定する必要があります。 `req=tmb` も指定されている場合は、エラーが返されます。

## 初期設定 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 関連項目 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
