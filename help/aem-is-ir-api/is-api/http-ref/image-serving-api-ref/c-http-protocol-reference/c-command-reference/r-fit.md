---
description: 応答の画像フィットモード。 倍率の計算方法を指定します。この値は、 wid=およびhei=で応答サイズが指定され、 scl=が存在しない場合に、合成画像を応答画像に合わせて拡大縮小するために使用されます。
solution: Experience Manager
title: フィット
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 2%

---

# フィット{#fit}

応答の画像フィットモード。 倍率の計算方法を指定します。この値は、 wid=およびhei=で応答サイズが指定され、 scl=が存在しない場合に、合成画像を応答画像に合わせて拡大縮小するために使用されます。

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

次のモードオプションの説明では、*`xScale`*&#x200B;が応答画像の幅に対する合成画像の幅の比率、*`yScale`*&#x200B;が応答画像の高さに対する合成画像の高さの比率であると仮定します。

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
   <td colname="col2"> <p><span class="codeph"> wid= </span>と<span class="codeph"> hei= </span>で割り当てられた領域に収まるように、合成画像を拡大/縮小します。空白は最小限で、切り抜きはありません。 応答画像のサイズは、<span class="codeph"> wid= </span>と<span class="codeph"> hei= </span>で指定したサイズになります。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>のうち小さい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 制約する  </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> fit </span>のような合成画像を、<span class="codeph"> wid= </span>と<span class="codeph"> hei= </span>で割り当てられた領域に収まるように拡大/縮小しますが、空白を避けるために、実際の応答画像は<span class="codeph"> wid= </span>と<span class="codeph"> hei= </span>で指定よりも小されます。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>のうち小さい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> 切り抜き </span> </p> </td> 
   <td colname="col2"> <p>最小限の切り抜きと空白を含めずに、応答画像全体を埋めるように合成画像を拡大縮小します。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>の大きい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> まとめる </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">切り抜き</span>のような複合画像を拡大/縮小して、応答画像全体を覆いますが、切り抜きを避けるために、実際の応答画像は<span class="codeph"> wid= </span>および<span class="codeph"> hei= </span>で指定したよりも大きくなる場合があります。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>の大きい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> ストレッチ  </span> </p> </td> 
   <td colname="col2"> <p>合成画像をxとyに独立して拡大/縮小し、切り抜きや空白を含めずに、応答画像全体を埋めます。 通常、画像の縦横比を変更します。 <span class="varname"> xScale </span> は、水平方向の拡大/縮小に使用し、yScaleは垂 <span class="varname"> 直方向 </span> の拡大/縮小に使用します。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> hit  </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> xScale </span>を適用して、画像を水平方向にきつく収め、トリミングや空白が上下に現れるようにします。 特殊な用途に役立ちます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit  </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> yScale </span>を適用して、画像を縦方向にきつく収め、切り抜きや空白を左右に配置します。 特殊な用途に役立ちます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`upscale`*&#x200B;を「1」に設定してアップスケーリングを許可するか、*`xScale`*および&#x200B;*`yScale`*&#x200B;を1:1に制限する場合は「0」に設定します。 アップスケーリングが無効になっている場合、複合画像が応答画像より小さい場合は、追加の空白が存在する可能性があります。

切り抜きと空白は、デフォルトで中央に配置されます。この位置は`align=`で制御できます。 空白の塗りの色と不透明度は`bgc=`で決まります。

## プロパティ {#section-6d7a5a7e18434bca9bc2fdb236af8909}

属性を表示します。 現在の画層設定に関係なく適用されます。 `wid=`または`hei=`の少なくとも1つを指定する必要があります。それ以外の場合は、エラーが返されます。フィットモードが説明どおりに動作するように、 `wid=`と`hei=`の両方を指定する必要があります。 `req=tmb`も指定されると、エラーが返されます。

## 初期設定 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 関連項目 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47) 、 [hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、 [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、 [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
