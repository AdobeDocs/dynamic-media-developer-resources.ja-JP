---
description: 画像を回転 画像、テキスト、またはべた塗りのレイヤーを指定した角度だけ回転します。
seo-description: 画像を回転 画像、テキスト、またはべた塗りのレイヤーを指定した角度だけ回転します。
seo-title: 循環
solution: Experience Manager
title: 循環
topic: Scene7 Image Serving - Image Rendering API
uuid: 160d3c4b-3871-43bd-a17d-96198c7ea839
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 4%

---


# rotate{#rotate}

画像を回転 画像、テキスト、またはべた塗りのレイヤーを指定した角度だけ回転します。

`rotate= *`角度`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 角度</span> </p> </td> 
  <td class="stentry"> <p>回転角度（度単位、実数） </p></td> 
 </tr> 
</table>

正の角度は時計回りに回転します。 レイヤーのアンカーポイント（`anchor=`または`catalog::Anchor`）が回転の中心となります。 必要に応じて、レイヤーの長方形を拡大し、回転したデータの周りにフィットさせて、切り抜きを防ぎます。 回転は、レイヤーの背景領域を`color=`で塗りつぶした後に適用されます。 `bgColor=` は、回転後に境界線の長方形に背景色を追加する場合に使用します。

## プロパティ {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

レイヤーコマンド 現在の画層に適用されます。`layer=comp`の場合は画層0に適用されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`に設定します。回転は行われません。

## 例 {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

画像カタログ内の画像の左上隅近くに「On Sale」ラベルを配置します。 ラベルの画像は300 x 300表示用に既に正しいサイズに設定されているので、左に30度回転する必要があります。 テキストボックスを白の半透明色で塗りつぶして、ラベルを強調します。

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

`size=`と`hei=`を使用する代わりに、レイヤ0に&lt;a0/>を適用して表示サイズを設定します。 `wid=`これにより、`myImageId`の最終的なサイズを変更せずに`labelImage`のサイズを変更できます。 また、`scl=1`を指定する必要があります。指定しないと、合成画像が`attribute::DefaultPix`に縮小される場合があります（0,0に設定されていない場合）。 `color=` 回転前に、テキストボックスに半透明の背景色を追加します。

両方のレイヤーの接触チャネルは、左上隅に設定され、目的の位置に合わせます。 レイヤー1の接触チャネル点は、回転後に`labelImage`に適用されます。

回転したテキストの例については、[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の[例A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac)を参照してください。

## 関連項目 {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
