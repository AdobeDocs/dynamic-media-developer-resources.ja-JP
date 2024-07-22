---
title: サイズ
description: レイヤーサイズ。 rotate=、perspective=、extend=をレイヤーに適用する前に、レイヤーのサイズまたは最大レイヤーサイズを指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---

# サイズ{#size}

レイヤーサイズ。 rotate=、perspective=、extend=をレイヤーに適用する前に、レイヤーのサイズまたは最大レイヤーサイズを指定します。

` size= *`width`*, *`height`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span>, <span class="varname"> height </span> </span> </p> </td> 
  <td class="stentry"> <p>レイヤーサイズの制限（ピクセル単位）（整数、整数、0 以上）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>レイヤー 0 サイズ（実数、実数、0.0...1.0）を基準にして正規化されたレイヤーサイズの制約。 </p> </td> 
 </tr> 
</table>

画像レイヤーに指定した場合、size=はレイヤーイメージの幅、高さ、またはその両方を制限します。 画像は `size=` 以下に拡大縮小されます。 正規化されたサイズが指定されている場合は、レイヤー 0 のサイズに対する相対サイズになります。 *`width`* と *`height`* の両方を指定した場合は、どのサイズも指定したサイズを超えないように、（`crop=` を適用した後に）ソース イメージのサイズが調整されます。 元の長方形の縦横比は、どの場合でも維持されます。 *`width`* または *`height`* のいずれかを 0 に設定できます。この場合、値は画像の縦横比に基づいてサーバーによって計算されます。

テキストレイヤーに対して指定した場合は、テキストボックスのサイズ `size=` 指定します。 *`width`* は必須です。*`height`* は 0 に設定できます。この場合、レイアウトされたテキストの高さがレイヤーの高さとして使用されます。 既定では、テキスト レイアウト エンジンは、テキストが常に使用可能なスペースに水平に収まるように改行を挿入します。 *`height`* を指定すると、使用可能なスペースに収まらない行は切り取られ（`text=`）、省略されます（`textPs=`）。 `text=` は、追加のフィット モードをサポートしています。詳細は、`textAttr=` を参照してください。

単色レイヤーに対して指定した場合、`size=` は正確なレイヤーサイズを定義します。両方の値を指定する必要があります（マスクが指定されていない場合）。 `mask=` も指定した場合は、イメージレイヤでイメージをスケールするのと同じ方法 `size=` 合わせて、マスクイメージのサイズが調整されます。

## プロパティ {#section-5f254b66fcba49bcb63f9c9ea40b230c}

レイヤー属性。 `layer=comp` の場合はレイヤー 0 に適用されます。 `sizeN=` は `layer=0` または `layer=comp` には許可されていません。 `sizeN=` は、透かし画像を定義するカタログレコードでのみ `layer=0` および `layer=comp` に使用できます。 この場合、`sizeN` は、透かしを適用する合成画像に対する透かし画像の拡大縮小を定義します。 `size=` が指定されている場合、`res=` と `scale=` はこのレイヤーで無視されます。 エフェクトレイヤーで無視されます。

## 初期設定 {#section-43d129deba6a441da66a1fdb63d1c85c}

ま `size=0,0`、レイヤーサイズは制限されません。 画像レイヤーの場合、`crop=`、`scale=`、`res=` のいずれかの操作が適用された後、レイヤーの画像サイズに基づいてレイヤーサイズが決定されます。 テキストレイヤーの場合、`size=` が指定されていないと、レンダリングされたテキストに合わせてレイヤーのサイズが自動的に調整されます。

単色レイヤーには、完全に指定された `size=`、`mask=`、`clipPath=` のいずれかが必要です。

## 例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) の [ 例 A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) を参照してください。

## 関連項目 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065)、[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55)、[textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d)、[mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e)、[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)、[ テキストレイヤー ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
