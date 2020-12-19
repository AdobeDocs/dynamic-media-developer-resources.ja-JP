---
description: レイヤーのサイズ rotate=、perspective=およびextend=をレイヤーに適用する前に、レイヤーのサイズまたは最大レイヤーサイズを指定します。
seo-description: レイヤーのサイズ rotate=、perspective=およびextend=をレイヤーに適用する前に、レイヤーのサイズまたは最大レイヤーサイズを指定します。
seo-title: サイズ
solution: Experience Manager
title: サイズ
topic: Scene7 Image Serving - Image Rendering API
uuid: c9c13062-7974-4dd9-aff4-f9502bcf442e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 1%

---


# サイズ{#size}

レイヤーのサイズ rotate=、perspective=およびextend=をレイヤーに適用する前に、レイヤーのサイズまたは最大レイヤーサイズを指定します。

` size= *``*, *`widthheight`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width  </span>、  <span class="varname"> height  </span> </span> </p> </td> 
  <td class="stentry"> <p>レイヤーサイズの制約（ピクセル単位、整数、0以上） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN  </span>、  <span class="varname"> heightN  </span> </span> </p> </td> 
  <td class="stentry"> <p>レイヤー0のサイズ（実数、実数、0.0 ～ 1.0）を基準に正規化されたレイヤーサイズコンストレイント。 </p> </td> 
 </tr> 
</table>

イメージレイヤに対して指定した場合、size=によってレイヤイメージの幅、高さ、またはその両方が制限されます。 画像は`size=`以下に拡大縮小されます。 正規化されたサイズを指定する場合、レイヤー0のサイズに対する相対サイズになります。 *`width`*&#x200B;と&#x200B;*`height`*&#x200B;の両方を指定した場合、`crop=`の適用後にソース画像が拡大/縮小され、どちらのサイズも指定したサイズを超えないようになります。 ソース長方形の縦横比は、すべての場合に維持されます。 *`width`*&#x200B;または&#x200B;*`height`*&#x200B;は0に設定できます。この場合、値は、画像の縦横比に基づいてサーバーによって計算されます。

テキストレイヤーに対して指定する場合、`size=`はテキストボックスのサイズを指定します。 *`width`* は必須です。 *`height`* は0に設定できます。0に設定した場合、レイアウトするテキストの高さがレイヤーの高さとして使用されます。デフォルトでは、テキストレイアウトエンジンは、テキストが常に水平方向に使用可能なスペースに収まるように改行を挿入します。 *`height`*&#x200B;を指定した場合、使用可能なスペースに収まらない行は、切り取られる(`text=`)か、省略されます(`textPs=`)。 `text=` は、その他のフィットモードをサポートします。詳細につ `textAttr=` いては、を参照してください。

べた塗りレイヤーに対して指定した場合、`size=`は正確なレイヤーサイズを定義します。両方の値を指定する必要があります（マスクを指定しない場合）。 `mask=`も指定した場合、マスク画像は、画像レイヤーで画像を拡大・縮小するのと同じ方法で、`size=`に合うようにサイズが調整されます。

## プロパティ {#section-5f254b66fcba49bcb63f9c9ea40b230c}

レイヤー属性。 `layer=comp`の場合にレイヤー0に適用されます。 `sizeN=` は、 `layer=0` またはに対しては許可されません `layer=comp`。`sizeN=` は、透かし画像を定義す `layer=0` るカタログレコードに対してのみ、また `layer=comp` はカタログレコードでのみ使用できます。この場合、`sizeN`は、透かしを適用する合成画像を基準にして透かし画像の尺度を定義します。 `size=`を指定した場合、`res=`と`scale=`はこのレイヤーでは無視されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`の場合、レイヤーサイズは拘束されません。次に、画像レイヤーの場合、`crop=`、`scale=`、または`res=`操作が適用された後のレイヤー画像サイズに基づいてレイヤーサイズが決定されます。 テキストレイヤーの場合、`size=`を指定しないと、レンダリングされたテキストに合わせてレイヤーのサイズが自動的に調整されます。

べた塗りレイヤーには、完全に指定された`size=`、`mask=`、または`clipPath=`が必要です。

## 例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の[例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)を参照してください。

## 関連項目 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ,  [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), mask= [, ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)clip  [Path=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) [, Path=, textLayers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
