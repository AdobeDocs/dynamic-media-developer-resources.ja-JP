---
description: 応答画像のフィットモード 倍率の計算方法を指定します。wid=およびhei=およびscl=を使用して応答サイズを指定した場合に、合成画像を応答画像に合わせて拡大・縮小するために使用されます。
seo-description: 応答画像のフィットモード 倍率の計算方法を指定します。wid=およびhei=およびscl=を使用して応答サイズを指定した場合に、合成画像を応答画像に合わせて拡大・縮小するために使用されます。
seo-title: フィット
solution: Experience Manager
title: フィット
topic: Scene7 Image Serving - Image Rendering API
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '525'
ht-degree: 2%

---


# フィット{#fit}

応答画像のフィットモード 倍率の計算方法を指定します。wid=およびhei=およびscl=を使用して応答サイズを指定した場合に、合成画像を応答画像に合わせて拡大・縮小するために使用されます。

` fit= *``*, *`modeupscale`*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> mode  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|crop|wrap|stretch|hfit|vfit  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> upscale  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

次のモードオプションの説明では、*`xScale`*&#x200B;が合成画像の幅と応答画像の幅との比率、*`yScale`*&#x200B;が合成画像の高さと応答画像の高さとの比率であると想定します。

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
   <td colname="col2"> <p><span class="codeph"> wid= </span>と<span class="codeph"> hei= </span>で割り当てられた領域に収まるように合成画像を拡大・縮小します。空白は最小限に抑え、切り抜きは不要です。 応答画像は、<span class="codeph"> wid= </span>と<span class="codeph"> hei= </span>で指定されたサイズと同じサイズになります。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>のうち小さい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 拘束する  </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">フィット</span>のように合成画像を拡大縮小して、<span class="codeph"> wid= </span>と<span class="codeph"> hei= </span>で割り当てられた領域に収まるようにします。ただし、空白を避けるため、実際の応答画像は<span class="codeph"> wid= </span>と<span class="codeph"> hei= </span>で指定するよりも小さくなります。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>のうち小さい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 切り抜き </span> </p> </td> 
   <td colname="col2"> <p>切り抜きを最小限に抑え、空白を含めずに、合成画像が応答画像全体に収まるように拡大縮小します。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>の大きい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> まとめる </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">切り抜き</span>のように合成画像を拡大縮小して応答画像全体に表示しますが、切り抜きを避けるために、実際の応答画像は<span class="codeph"> wid= </span>および<span class="codeph"> hei= </span>で指定された値より大きくなる場合があります。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>の大きい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 伸ばす  </span> </p> </td> 
   <td colname="col2"> <p>合成画像をxおよびy方向に個別に拡大・縮小して、切り抜きや空白なしで、応答画像全体を埋めます。 通常、これにより画像の縦横比が変更されます。 <span class="varname"> xScale </span> は水平方向の拡大縮小に使用され、 <span class="varname"> yScaleは垂直方向 </span> の拡大縮小に使用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hift  </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> xScale </span>を適用して、画像を水平方向にぴったりと合わせます。上部や下部に切り抜きや空白が表示される可能性があります。 特殊な用途に役立ちます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit  </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> yScale </span>を適用して、画像を縦にぴったりと合わせます。左または右に切り抜きや空白が表示される可能性があります。 特殊な用途に役立ちます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`upscale`*&#x200B;を&#39;1&#39;に設定して拡大を許可するか、*`xScale`*および&#x200B;*`yScale`*&#x200B;を1:1に制限する場合は&#39;0&#39;に設定します。 拡大縮小を無効にすると、複合画像が応答画像より小さい場合に、空白が表示される場合があります。

切り抜きと空白はデフォルトで中央に配置されます。この位置は`align=`で制御できます。 空白の塗りの色と不透明度は、`bgc=`によって決まります。

## プロパティ {#section-6d7a5a7e18434bca9bc2fdb236af8909}

表示属性。 現在のレイヤー設定に関係なく適用されます。 `wid=`または`hei=`の少なくとも1つを指定する必要があります。指定しない場合はエラーが返されます。はめあいモードが説明どおりに動作するには、`wid=`と`hei=`の両方を指定する必要があります。 `req=tmb`も指定すると、エラーが返されます。

## 初期設定 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 関連項目 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 、 [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、 [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
