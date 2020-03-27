---
description: 応答画像のフィットモード wid=およびhei=およびscl=で応答サイズが指定されていない場合に、合成画像を応答画像に合わせて拡大・縮小するために使用される、拡大・縮小率の計算方法を指定します。
seo-description: 応答画像のフィットモード wid=およびhei=およびscl=で応答サイズが指定されていない場合に、合成画像を応答画像に合わせて拡大・縮小するために使用される、拡大・縮小率の計算方法を指定します。
seo-title: フィット
solution: Experience Manager
title: フィット
topic: Scene7 Image Serving - Image Rendering API
uuid: 669fe757-f3a1-4cd4-b46c-6fbe5a039ce0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# フィット{#fit}

応答画像のフィットモード wid=およびhei=およびscl=で応答サイズが指定されていない場合に、合成画像を応答画像に合わせて拡大・縮小するために使用される、拡大・縮小率の計算方法を指定します。

` fit= *`modeupscale`*, *``*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> モー </span> ド </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|crop|wrap|stretch|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 高 </span> 級 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
 </tr> 
</table>

次のモードオプションの説明では、合成画像の幅と応答画像の幅との比を示し、合成画像の高さと応答画像の高さの比を示し *`xScale`**`yScale`* ていると想定されます。

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
   <td colname="col2"> <p>wid=とhei=で割り当てられた領域に収まるように、合成画像を拡大・縮小します。空 <span class="codeph"> 白は最小限 </span> で、切り <span class="codeph"></span>抜きは行われません。 応答画像は、 <span class="codeph"> wid=とhei=で指定されたとお </span> りのサ <span class="codeph"> イズになりま </span>す。 xScaleとyScaleの値が小さ <span class="varname"> い方が </span> 適用さ <span class="varname"> れ </span> ます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 拘束する </span> </p> </td> 
   <td colname="col2"> <p>合成画像を <span class="codeph"> fit </span> のように拡大・縮小し、wid=とhei=で割り当てられた領域に収まるようにしますが、実際の応答は <span class="codeph"> wid=とhei=で割り当てられた領域より小さく、hei=と空白を避ける </span><span class="codeph"></span><span class="codeph"></span><span class="codeph"></span> ようにします。 xScaleとyScaleの値が小さ <span class="varname"> い方が </span> 適用さ <span class="varname"> れ </span> ます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 切り抜き </span> </p> </td> 
   <td colname="col2"> <p>切り抜きを最小限に抑え、空白を含めずに、応答画像全体を埋めるように合成画像を拡大・縮小します。 xScaleとyScaleの大き <span class="varname"> い方が </span> 適用さ <span class="varname"> れ </span> ます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> まとめる </span> </p> </td> 
   <td colname="col2"> <p>合成画像を切り抜きのよ <span class="codeph"> うに </span> 拡大・縮小して応答画像全体を覆いますが、切り抜きを避けるために、実際の応答画像は <span class="codeph"> wid=とhei=で指定した値より大きくなる場合が </span><span class="codeph"></span> あります。 xScaleとyScaleの大き <span class="varname"> い方が </span> 適用さ <span class="varname"></span>れます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> ストレッチ </span> </p> </td> 
   <td colname="col2"> <p>合成画像をxとyで個別に拡大・縮小し、応答画像全体を埋めます。切り抜きや空白は使用しません。 通常、これは画像の縦横比を変更します。 <span class="varname"> xScaleは水 </span> 平方向の拡大・縮小に使用され、yScaleは <span class="varname"> 垂直方向の </span> 拡大・縮小に使用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hift </span> </p> </td> 
   <td colname="col2"> <p>xScaleを適 <span class="varname"> 用し </span> て、画像を水平方向にぴったりと収め、切り抜きや空白を上下に並べます。 特殊な用途に役立ちます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>画像を <span class="varname"> 縦に </span> ぴったりと収まるようにyScaleを適用します。左または右に切り抜きや空白がある可能性があります。 特殊な用途に役立ちます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

拡大を許 *`upscale`* 可するには&#39;1&#39;に設定し、**を制限するには&#39;0&#39;に設定し、`xScale`*`yScale`* 1:1に制限します。 アップスケールが無効な場合、複合画像が応答画像より小さい場合は、空白が表示される場合があります。

切り抜きと空白は、デフォルトで中央に配置されます。その位置は、を使用して制御できま `align=`す。 空白の塗りの色と不透明度は、によって決まりま `bgc=`す。

## プロパティ {#section-6d7a5a7e18434bca9bc2fdb236af8909}

属性を表示します。 現在のレイヤー設定に関係なく適用されます。 またはの少なくとも1つを指 `wid=` 定する必 `hei=` 要があります。それ以外の場合はエラーが返されます。はめあい `wid=` モードが説 `hei=` 明どおりに動作するように、とを指定する必要があります。 が指定された場合も、エ `req=tmb` ラーが返されます。

## 初期設定 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 関連項目 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) , [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
