---
description: レイヤーサイズ。 回転=、パースペクティブ=、および延長=をレイヤに適用する前の、レイヤのサイズまたは最大レイヤサイズを指定します。
solution: Experience Manager
title: サイズ
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 1%

---

# サイズ{#size}

レイヤーサイズ。 回転=、パースペクティブ=、および延長=をレイヤに適用する前の、レイヤのサイズまたは最大レイヤサイズを指定します。

` size= *``*, *`widthheight`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width  </span>,  <span class="varname"> height  </span> </span> </p> </td> 
  <td class="stentry"> <p>レイヤーサイズの制約（ピクセル単位、整数、0以上）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN  </span>、  <span class="varname"> heightN  </span> </span> </p> </td> 
  <td class="stentry"> <p>レイヤーの0サイズ（実数、実数、0.0 ～ 1.0）に対して正規化されたレイヤーサイズの制約。 </p> </td> 
 </tr> 
</table>

画像レイヤーに対してsize=を指定すると、レイヤー画像の幅または高さ、またはその両方が制限されます。 画像は`size=`以下に拡大縮小されます。 正規化されたサイズを指定した場合、レイヤー0のサイズに対する相対サイズになります。 *`width`*&#x200B;と&#x200B;*`height`*&#x200B;の両方を指定した場合は、`crop=`の適用後にソース画像が拡大/縮小され、指定したサイズを超えないようになります。 ソース長方形の縦横比は、どの場合でも維持されます。 *`width`*&#x200B;または&#x200B;*`height`*&#x200B;は0に設定できます。この場合、値はサーバーによって画像の縦横比に基づいて計算されます。

テキストレイヤーに対して`size=`を指定すると、テキストボックスのサイズが指定されます。 *`width`* は必須です。 *`height`* は0に設定でき、レイアウトされたテキストの高さがレイヤーの高さとして使用されます。デフォルトでは、テキストレイアウトエンジンは改行を挿入し、テキストが常に使用可能なスペース内に水平方向に収まるようにします。 *`height`*&#x200B;を指定した場合、空きスペースに収まらない行は切り詰められるか(`text=`)、省略されます(`textPs=`)。 `text=` は、追加のフィットモードをサポートします。詳しくは、を参 `textAttr=` 照してください。

べた塗りのレイヤーに対して指定した場合、`size=`は正確なレイヤーサイズを定義します。両方の値を指定する必要があります（マスクを指定しない限り）。 `mask=`も指定した場合、画像レイヤーで画像を拡大縮小するのと同じ方法で、`size=`に合わせてマスク画像のサイズが調整されます。

## プロパティ {#section-5f254b66fcba49bcb63f9c9ea40b230c}

レイヤー属性。 `layer=comp`の場合はレイヤ0に適用されます。 `sizeN=` またはに対しては許可さ `layer=0` れていま `layer=comp`せん。`sizeN=` は、透かし画像を定 `layer=0` 義す `layer=comp` るカタログレコードでのみ、およびに対して許可されます。この場合、`sizeN`は、透かしが適用される合成画像を基準にした透かし画像の拡大/縮小を定義します。 `size=`を指定した場合、このレイヤーでは`res=`と`scale=`は無視されます。 エフェクトレイヤでは無視されます。

## 初期設定 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`の場合、レイヤーサイズは拘束されません。次に、画像レイヤの場合、`crop=`、`scale=`または`res=`の処理が適用された後のレイヤ画像サイズに基づいて、レイヤサイズが決定されます。 テキストレイヤーの場合、 `size=`を指定しないと、レイヤーのサイズはレンダリングされたテキストに合わせて自動的に調整されます。

ソリッドカラーレイヤーには、完全に指定された`size=`、`mask=`、`clipPath=`が必要です。

## 例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

[[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)を参照してください。

## 関連項目 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) 、 [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55)、 [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)、 [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)、 [Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
