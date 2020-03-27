---
description: 画像を回転 画像、テキストまたはべた塗りのレイヤーを指定した角度だけ回転させます。
seo-description: 画像を回転 画像、テキストまたはべた塗りのレイヤーを指定した角度だけ回転させます。
seo-title: 循環
solution: Experience Manager
title: 循環
topic: Scene7 Image Serving - Image Rendering API
uuid: 160d3c4b-3871-43bd-a17d-96198c7ea839
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# rotate{#rotate}

画像を回転 画像、テキストまたはべた塗りのレイヤーを指定した角度だけ回転させます。

`rotate= *`角度`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 角度</span> </p> </td> 
  <td class="stentry"> <p>回転角度（度単位、実数） </p></td> 
 </tr> 
</table>

正の角度は時計回りに回転します。 レイヤーのアンカーポイ `anchor=` ント(ま `catalog::Anchor`たは)が回転の中心となります。 切り抜きを避けるために、必要に応じて、レイヤーの長方形を拡大し、回転したデータの周りに合わせます。 回転は、レイヤーの背景領域を塗りつぶした後に適用されま `color=`す。 `bgColor=` を使用して、回転後に境界の長方形に背景色を追加できます。

## プロパティ {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

レイヤーコマンド 現在のレイヤに適用されます。レイヤ0の場合は適用されま `layer=comp`す。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`を指定します。回転は使用しません。

## 例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

画像カタログ内の画像の左上隅近くに「On Sale」ラベルを配置します。 ラベルの画像は300 x 300のビューに対しては既に正しいサイズになっており、左に30度回転させる必要があります。 テキストボックスを白の半不透明色で塗りつぶし、ラベルを強調します。

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

とを使用す `size=` る代わりに、レイヤ0に適用してビューサイズを設定し `wid=` ます `hei=`。 これにより、の最 `myImageId` 終的なサイズを変更せずに、サイズを変更できま `labelImage`す。 また、を指定する必要があ `scl=1`ります。指定しない場合、合成画像は0,0に設定さ `attribute::DefaultPix` れていない限り、拡大・縮小される可能性があります。 `color=` 回転前に、テキストボックスに半不透明の背景色を追加します。

両方のレイヤーの原点は、目的の位置揃えを行うために、左上隅に設定されます。 レイヤー1の原点は、回転後に適 `labelImage`用されます。

回転し [たテキストの例につ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) いては [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) 、Example A in Templatesを参照してください。

## 関連項目 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) , [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
