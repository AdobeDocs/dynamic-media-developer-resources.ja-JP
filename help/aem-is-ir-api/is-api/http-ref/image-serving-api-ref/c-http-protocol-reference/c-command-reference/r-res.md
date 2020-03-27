---
description: 解像度ベースの画像の拡大・縮小 画像を要求された解像度に拡大・縮小します。
seo-description: 解像度ベースの画像の拡大・縮小 画像を要求された解像度に拡大・縮小します。
seo-title: res
solution: Experience Manager
title: res
topic: Scene7 Image Serving - Image Rendering API
uuid: ab0c8329-5d40-4233-a122-8cb8ca01b500
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# res{#res}

解像度ベースの画像の拡大・縮小 画像を要求された解像度に拡大・縮小します。

` res= *`val`*`

<table id="simpletable_E69F3709266749C4A165C90FF18FF5AA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>目標解像度；通常は、ppi（実数）で表します。 </p> </td> 
 </tr> 
</table>

スケール係数は、で割って計算さ *`val`* れま `catalog::Resolution`す。 このコマンドは、返信画像の印刷解像度には影響しません。

この機能を使用するには、元のソース画像の解像度を確認し、で設定する必要がありま `catalog::Resolution`す。 アプリケーションによっては、解像度の単位が異なる場合があります。 繰り返し可能な2Dテクスチャやマテリアルスウォッチ（壁紙や布地など）の場合、解像度はピクセル/インチ(pixel/inch)またはピクセル/mm(mm)で表すことができます。 航空写真や地図は、ピクセル/マイルまたはピクセル/kmで配信した方がよいでしょう。 いずれの場合も、に使用する単位は、に使 `catalog::Resolution` 用する単位と同じである必要がありま `res=`す。

また、正確な解像度で画像を取得する以外に `res=` 、複数の画像を同じ解像度で組み合わせて、画像に表示される項目を互いに正確に比例させることもできます。

>[!NOTE]
>
>通常、合成画像は、クライアントに返される前に、(、またはで指定さ `wid=`れた) `hei=`ターゲットビ `attribute::DefaultPix`ューサイズに合わせてサイズ変更されます。 このサイズ変更を防ぎ、で指定した正確な解像度の画像を取得するには、明示的に指定し `res=`てビューの拡大/縮小を無効にする必要がある場合がありま `scl=1`す。 これにより、サーバは、合成画像を拡大・縮小するのではなく、ターゲットのビューサイズに合わせて切り抜くようになります。

## プロパティ {#section-fdbd16e59cff4952a3717146bc91412e}

ソース画像/マスク属性。 ソース画像またはマスクに関連付けられていないレイヤーでは無視されます。 レイヤー0に適用が指定されまし `layer=comp`た。 同じレイヤーに対し `scale=` てまたは `size=` が指定されている場合は無視されます。

## 初期設定 {#section-c5f1ba6fe53d46eca32e7d0588dcdf3d}

指定しなかった場合、ま `scale=` たは `size=` 尺度係数を指定した場合、または指定しなかった場合は、画像が拡大・縮小せずに使用されます。

## 例 {#section-eb06f333e08e4247971fb1b18922597b}

12ピクセル/インチのオブジェクト解像度でテクスチャ画像を取得し、画像レンダリングまたは画像オーサリングで使用します。 損失のないPNG形式を指定し、最高の画質を得るためにより高い画質でリサンプリングを行います。

` http:// *`server`*/myTexture?res=12&fmt=png&resMode=sharp`

## 関連項目 {#section-1f8a8f11772e493ca803c4511f397a11}

[catalog::Resolution](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-resolution-cat.md#reference-de489f5f36b64bd0831749546f8728e1)[,](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1)attribute::DefaultPix [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc)scl= [, fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a)
