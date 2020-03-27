---
description: レイヤーのサイズ 回転=、遠近法=、および延長=をレイヤーに適用する前に、レイヤーのサイズまたは最大レイヤーサイズを指定します。
seo-description: レイヤーのサイズ 回転=、遠近法=、および延長=をレイヤーに適用する前に、レイヤーのサイズまたは最大レイヤーサイズを指定します。
seo-title: サイズ
solution: Experience Manager
title: サイズ
topic: Scene7 Image Serving - Image Rendering API
uuid: c9c13062-7974-4dd9-aff4-f9502bcf442e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# サイズ{#size}

レイヤーのサイズ 回転=、遠近法=、および延長=をレイヤーに適用する前に、レイヤーのサイズまたは最大レイヤーサイズを指定します。

` size= *`幅の`*, *`高さ`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 幅、 </span>高さ <span class="varname"></span></span> </p> </td> 
  <td class="stentry"> <p>レイヤーサイズの制約（ピクセル単位、整数、0以上）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>、 <span class="varname"> height </span> N </span> </p> </td> 
  <td class="stentry"> <p>レイヤー0のサイズ（実数、実数、0.0 ～ 1.0）を基準に正規化されたレイヤーサイズ制約。 </p> </td> 
 </tr> 
</table>

画像レイヤーに対してsize=を指定すると、レイヤー画像の幅、高さ、またはその両方が制限されます。 画像は、以下の大きさに縮小されます `size=`。 正規化されたサイズを指定した場合、レイヤー0のサイズを基準とした相対サイズになります。 との両方を指 *`width`* 定した場 *`height`* 合、どちらのサイズも指定したサイズを超えないように、ソー `crop=` ス画像が（適用後に）拡大/縮小されます。 元の長方形の縦横比はすべての場合に維持されます。 または0 *`width`* に設 *`height`* 定することができます。この場合、画像の縦横比に基づいてサーバが値を計算します。

テキストレイヤーに対して指定する場合は、テキ `size=` ストボックスのサイズを指定します。 *`width`* は必須です。は0に設 *`height`* 定できます。0の場合、レイアウトテキストの高さがレイヤーの高さとして使用されます。 デフォルトでは、テキストレイアウトエンジンは、テキストが常に水平方向に使用可能なスペースに収まるように改行を挿入します。 を指 *`height`* 定すると、使用可能なスペースに収まらない行は切り取られる( `text=`)か、省略され `textPs=`る()。 `text=` は、追加のフィットモードをサポートします。詳しくは、を参照 `textAttr=` してください。

べた塗りレイヤーに対して指定する場合、正確な `size=` レイヤーサイズを定義します。両方の値を指定する必要があります（マスクを指定しない場合）。 も指定 `mask=` した場合、マスク画像は、画像レイヤーで画像が拡大・縮小されるのと同じ方 `size=` 法で収まるようにサイズ調整されます。

## プロパティ {#section-5f254b66fcba49bcb63f9c9ea40b230c}

レイヤー属性。 レイヤー0の場合に適用されま `layer=comp`す。 `sizeN=` またはに対しては許可され `layer=0` ませ `layer=comp`ん。 `sizeN=` は、透かし画像を定 `layer=0` 義するカ `layer=comp` タログレコードに対してのみ使用できます。 この場合、透かし `sizeN` を適用する合成画像を基準にして、透かし画像の拡大縮小を定義します。 を指定 `size=` した場合、この `res=` レイヤー `scale=` では無視されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`の場合、レイヤーサイズは制限されません。 次に、画像レイヤーの場合、レイヤーのサイズは、適用後のレイヤー画像のサ `crop=`イズに基 `scale=`づいて決 `res=` 定されます。 テキストレイヤーの場合、この `size=` オプションを指定しないと、レンダリングされたテキストに合わせてレイヤーのサイズが自動的に調整されます。

べた塗りレイヤーには、完全に指定された、またはのい `size=`ずれかが `mask=`必要になりま `clipPath=`す。

## 例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

詳しくは、 [Example A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Templatesを参照してください](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 関連項目 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [res,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)cripPath= [,](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)[textLayers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
