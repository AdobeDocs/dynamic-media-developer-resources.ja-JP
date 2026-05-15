---
title: フィット
description: 応答画像の適合モード。 応答サイズをwid=とhei=で指定し、scl=が存在しない場合に、合成画像を応答画像に拡大・縮小するために使用するスケール係数の計算方法を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d2939f86-5dab-471d-ba59-70d91ae1e4fd
TQID: 'https://experienceleague.adobe.com/qCi-M0u1lJZ2SSc3bnezs1jjpXhcqsv-pKCvQ60XSo8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 488
ht-degree: 1%

---

# フィット{#fit}

応答画像の適合モード。 応答サイズをwid=とhei=で指定し、scl=が存在しない場合に、合成画像を応答画像に拡大・縮小するために使用するスケール係数の計算方法を指定します。

` fit= *` モード `*, *` アップスケール `*`

<table id="simpletable_50FBDC6B7CB2448891DD0F491DEB5ACF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> モード </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fit|constrain|crop|wrap|stretch|hfit|vfit </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> アップスケール </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
 </tr> 
</table>

次のモードオプションの説明では、*`xScale`*&#x200B;は合成画像の幅と応答画像の幅の比率であり、*`yScale`*&#x200B;は合成画像の高さと応答画像の高さの比率であると仮定します。

<table id="table_33408ECA9D164AFAA249F8589060545E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> パラメータ </th> 
   <th colname="col2" class="entry"> 定義 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">適合</span> </p> </td> 
   <td colname="col2"> <p>合成イメージを拡大・縮小して、<span class="codeph"> wid= </span>および<span class="codeph"> hei= </span>で割り当てられたスペースに収まるようにします。空白は最小限に抑え、切り抜きは行いません。 応答イメージは、<span class="codeph"> wid= </span>および<span class="codeph"> hei= </span>で指定された正確なサイズです。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>の小さい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">制約</span> </p> </td> 
   <td colname="col2"> <p><span class="codeph">のような合成画像を</span>に合わせてのように拡大・縮小し、<span class="codeph"> wid= </span>および<span class="codeph"> hei= </span>で割り当てられたスペースに収まるようにします。ただし、実際の応答画像は、<span class="codeph"> wid= </span>および<span class="codeph"> hei= </span>で指定したサイズよりも小さい場合があり、空白を避けることができます。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>の小さい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph">切り抜き</span> </p> </td> 
   <td colname="col2"> <p>合成画像を拡大・縮小して、レスポンス画像全体を塗りつぶし、トリミングを最小限に抑え、空白を含めないようにします。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>の大きい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> </span>をラップ </p> </td> 
   <td colname="col2"> <p><span class="codeph">切り抜き</span>のように合成画像を拡大/縮小して、応答画像全体をカバーしますが、実際の応答画像は、<span class="codeph"> wid= </span>および<span class="codeph"> hei= </span>で指定したサイズよりも大きくして、切り抜きを避けることができます。 <span class="varname"> xScale </span>と<span class="varname"> yScale </span>の大きい方が適用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> ストレッチ </span> </p> </td> 
   <td colname="col2"> <p>合成イメージをxとyに個別に拡大・縮小して、切り抜きや空白を含めずにレスポンス画像全体を塗りつぶします。 これは通常、画像の縦横比を変更します。 <span class="varname"> xScale </span>は水平方向の拡大・縮小に使用され、垂直方向の拡大・縮小には<span class="varname"> yScale </span>が使用されます。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> ヒット </span> </p> </td> 
   <td colname="col2"> <p><span class="varname"> xScale </span>を適用して、画像を水平方向に厳密にフィットさせ、上下にトリミングまたはホワイトスペースを配置します。 特殊な用途に便利。 </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> vfit </span> </p> </td> 
   <td colname="col2"> <p>画像を垂直方向に厳密に収めるように<span class="varname">拡大・縮小</span>を適用します。左または右にトリミングまたは空白が発生する可能性があります。 特殊な用途に便利。 </p> </td> 
  </tr> 
 </tbody> 
</table>

*`upscale`*&#x200B;を「1」に設定してアップスケーリングを許可するか、*`xScale`*と&#x200B;*`yScale`*&#x200B;を制限して1:1を制限する「0」に設定します。 アップスケーリングが無効になっている場合、合成画像が応答画像よりも小さい場合、余白が追加される可能性があります。

切り抜きと空白はデフォルトで中央に配置されます。位置は`align=`で制御できます。 空白の塗りの色と不透明度は、`bgc=`によって決まります。

## プロパティ {#section-6d7a5a7e18434bca9bc2fdb236af8909}

ビュー属性。 現在のレイヤー設定に関係なく適用されます。 `wid=`または`hei=`の少なくとも1つを指定する必要があります。そうしないと、エラーが返されます。説明どおりに動作させるには、`wid=`と`hei=`の両方を指定する必要があります。 `req=tmb`が指定された場合もエラーが返されます。

## 初期設定 {#section-3a553b4b29ef447a8331d6954f3f06da}

`fit=fit,0`

## 関連項目 {#section-788f7e168da64fc5abf29d971a598b01}

[wid=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-wid.md#reference-bfeadcb67bf4485f851eb21345527e47)、[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96)、[scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)、[align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7)
