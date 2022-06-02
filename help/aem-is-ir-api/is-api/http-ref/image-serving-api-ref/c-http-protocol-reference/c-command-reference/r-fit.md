---
title: フィット
description: 応答の画像フィットモード。 尺度係数の計算方法を指定します。この値は、 wid=および hei=および scl=で応答サイズが指定されていない場合に、合成画像を応答画像に合わせて尺度変更するために使用されます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '486'
ht-degree: 2%

---

# フィット{#fit}

応答の画像フィットモード。 尺度係数の計算方法を指定します。この値は、 wid=および hei=および scl=で応答サイズが指定されていない場合に、合成画像を応答画像に合わせて尺度変更するために使用されます。

` fit= *`mode`*, *`アップスケール`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mode </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|crop|wrap|stretch|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> アップスケール </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

以下のモードオプションの説明では、 *`xScale`* は、合成画像の幅と応答画像の幅の比率です。 *`yScale`* は、合成画像の高さと応答画像の高さの比率です。

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> パラメータ </th> 
   <th colname="col2" class="entry"> 定義 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> フィット </span> </p> </td> 
   <td colname="col2"> <p>合成イメージを、 <span class="codeph"> wid= </span> および <span class="codeph"> hei= </span>空白を最小限に抑え、切り抜きをおこないません。 応答画像のサイズは、 <span class="codeph"> wid= </span> および <span class="codeph"> hei= </span>. より小さい <span class="varname"> xScale </span> および <span class="varname"> yScale </span> が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 制約する </span> </p> </td> 
   <td colname="col2"> <p>次のように合成画像を拡大・縮小します。 <span class="codeph"> フィット </span> それは、 <span class="codeph"> wid= </span> および <span class="codeph"> hei= </span>が返されますが、実際の応答画像は、 <span class="codeph"> wid= </span> および <span class="codeph"> hei= </span> 空白を避けるため。 より小さい <span class="varname"> xScale </span> および <span class="varname"> yScale </span> が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 切り抜き </span> </p> </td> 
   <td colname="col2"> <p>最小限の切り抜きと空白を含めずに、応答画像全体を埋めるように合成画像を拡大・縮小します。 大きい <span class="varname"> xScale </span> および <span class="varname"> yScale </span> が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> まとめる </span> </p> </td> 
   <td colname="col2"> <p>次のように合成画像を拡大・縮小します。 <span class="codeph"> 切り抜き </span> 応答画像全体をカバーするようにしますが、実際の応答画像は、 <span class="codeph"> wid= </span> および <span class="codeph"> hei= </span> 切り抜きを避けるため。 大きい <span class="varname"> xScale </span> および <span class="varname"> yScale </span>が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> ストレッチ </span> </p> </td> 
   <td colname="col2"> <p>合成画像を x と y で個別に拡大/縮小し、切り抜きや空白を含めずに、応答画像全体を埋めます。 通常、これにより画像の縦横比が変更されます。 <span class="varname"> xScale </span> は水平方向の拡大/縮小に使用され、 <span class="varname"> yScale </span> 垂直方向の拡大/縮小に使用します。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hit </span> </p> </td> 
   <td colname="col2"> <p>適用 <span class="varname"> xScale </span> 画像を水平方向にきつく合わせ、切り抜きや空白が上部や下部に表示されるようにします。 特殊なアプリケーションに役立ちます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>適用 <span class="varname"> yScale </span> 左右に切り抜きや空白が生じやすく、画像を縦にぴったりと合わせる。 特殊なアプリケーションに役立ちます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定 *`upscale`* を「1」に設定するか、「0」に設定して制限します*`xScale`*および *`yScale`* を 1:1 に制限します。 アップスケーリングが無効になっている場合、複合画像が応答画像より小さい場合は、空白が追加で存在する可能性があります。

切り抜きと空白文字は、デフォルトで中央揃えになります。位置は、 `align=`. 空白の塗りの色と不透明度は、 `bgc=`.

## プロパティ {#section-6d7a5a7e18434bca9bc2fdb236af8909}

属性を表示します。 現在の画層設定に関係なく適用されます。 少なくとも 1 つの `wid=` または `hei=` また、を指定する必要があります。指定しない場合は、エラーが返されます。両方 `wid=` および `hei=` は、フィットモードが説明どおりに動作するように指定する必要があります。 次の場合にエラーが返されます。 `req=tmb` も指定されます。

## 初期設定 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 関連項目 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
