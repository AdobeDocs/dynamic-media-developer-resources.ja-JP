---
description: レイヤーサイズ。 回転=、パースペクティブ=、および extend=がレイヤーに適用される前の、レイヤーのサイズまたは最大レイヤーサイズを指定します。
solution: Experience Manager
title: サイズ
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '418'
ht-degree: 1%

---

# サイズ{#size}

レイヤーサイズ。 回転=、パースペクティブ=、および extend=がレイヤーに適用される前の、レイヤーのサイズまたは最大レイヤーサイズを指定します。

` size= *`幅`*, *`高さ`*`

` sizeN= *`widthN`*, *`heightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 幅 </span>, <span class="varname"> 高さ </span> </span> </p> </td> 
  <td class="stentry"> <p>レイヤーサイズの制約（ピクセル単位、整数、0 以上）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> widthN </span>, <span class="varname"> heightN </span> </span> </p> </td> 
  <td class="stentry"> <p>レイヤー 0 のサイズ（実数、実数、0.0 ～ 1.0）を基準に正規化されたレイヤーサイズの制約。 </p> </td> 
 </tr> 
</table>

画像レイヤーに対して size=を指定すると、レイヤー画像の幅や高さ、またはその両方が制限されます。 画像は以下に拡大縮小されます `size=`. 正規化されたサイズを指定した場合、レイヤー 0 のサイズを基準とした相対サイズになります。 両方の *`width`* および *`height`* を指定した場合、ソース画像は拡大・縮小されます ( `crop=` が適用される ) ので、指定したサイズを超える寸法はありません。 ソース長方形の縦横比は、どの場合でも維持されます。 次のいずれか *`width`* または *`height`* は 0 に設定できます。この場合、値は画像の縦横比に基づいてサーバーによって計算されます。

テキストレイヤーに対して指定する場合、 `size=` テキストボックスのサイズを指定します。 *`width`* は必須です。 *`height`* は 0 に設定でき、レイアウトされたテキストの高さがレイヤーの高さとして使用されます。 デフォルトでは、テキストレイアウトエンジンは改行を挿入し、テキストが常に使用可能なスペース内に水平方向に収まるようにします。 If *`height`* が指定されている場合、使用可能なスペースに収まらない行は切り取られます ( `text=`) または省略 ( `textPs=`) をクリックします。 `text=` は、追加のフィットモードをサポートします。参照する `textAttr=` 」を参照してください。

べた塗りレイヤーに対して指定する場合、 `size=` 正確なレイヤーサイズを定義します。両方の値を指定する必要があります（マスクが指定されていない場合）。 If `mask=` を指定した場合は、マスク画像のサイズが `size=` 同じ方法で、画像レイヤーで画像を拡大・縮小できます。

## プロパティ {#section-5f254b66fcba49bcb63f9c9ea40b230c}

レイヤー属性。 次の場合にレイヤー 0 に適用 `layer=comp`. `sizeN=` 次に対して許可されていません： `layer=0` または `layer=comp`. `sizeN=` は次の場合に許可されています： `layer=0` および `layer=comp` 透かし画像を定義するカタログレコード内のみ。 この場合、 `sizeN` 透かしを適用する合成画像を基準とした透かし画像の拡大/縮小を定義します。 If `size=` が指定されている場合、 `res=` および `scale=` は、この画層では無視されます。 効果画層で無視されます。

## 初期設定 {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`を指定した場合、レイヤーサイズは拘束されません。 次に、画像レイヤーの場合、レイヤーサイズは、後のレイヤー画像サイズに基づいて決定されます `crop=`, `scale=`または `res=` 操作が適用されました。 テキストレイヤーの場合、 `size=` を指定しない場合、レンダリングされたテキストに合わせてレイヤのサイズが自動的に調整されます。

べた塗りのレイヤーには、完全に指定された `size=`, a `mask=`または `clipPath=`.

## 例 {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

詳しくは、 [例 A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## 関連項目 {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) , [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55), [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d), [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), [テキストレイヤー](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
