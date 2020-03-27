---
description: 画像アンカー 変換（切り抜き、拡大・縮小、回転、反転）を適用する前に、画像、べた塗り、またはテキストバウンディングボックスの長方形のアンカーポイントを定義します。 また、rotate=の回転の中心としても使用されます。
seo-description: 画像アンカー 変換（切り抜き、拡大・縮小、回転、反転）を適用する前に、画像、べた塗り、またはテキストバウンディングボックスの長方形のアンカーポイントを定義します。 また、rotate=の回転の中心としても使用されます。
seo-title: アンカー
solution: Experience Manager
title: アンカー
topic: Scene7 Image Serving - Image Rendering API
uuid: 3b174360-9bb7-4dc8-83be-6b8c4ea88cd4
translation-type: tm+mt
source-git-commit: fe557a2429ceb7b48f22b9cbef5820ad39bad69f

---


# アンカー{#anchor}

画像アンカー 変換（切り抜き、拡大・縮小、回転、反転）を適用する前に、画像、べた塗り、またはテキストバウンディングボックスの長方形のアンカーポイントを定義します。 また、rotate=の回転の中心としても使用されます。

`anchor= *`コード`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> コー <span class="varname"> ド</span></span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上隅からのピクセルオフセット(int、int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span></span> </p> </td> 
  <td class="stentry"> <p>ソース画像の中心からの正規化されたオフセット（実数、実数） </p></td> 
 </tr> 
</table>

アンカーポイントは画像で変換され、レイヤーの原点になります(この場合は、が指定されていない限り、回転の中心とし `origin=` てのみ使用されま `anchor=``rotate=`す)。

`anchorN=0,0` ソース画像の中央に画像アンカーを配置します。 `anchorN=-0.5,-0.5` また `anchor=0,0` は、がソース画像の左上隅 `anchorN=0.5,0.5` 、および右下隅にある場合。

## プロパティ {#section-f08942bc6aae46a8b5d341faaff80640}

ソース画像属性。 現在のレイヤに適用されます。レイヤ0の場合は適用されま `layer=comp`す。

## 初期設定 {#section-35d369fab1254f1a9b91684a6e169ad1}

を指 `anchor=` 定しない場合、catalog::Anchorが使用されます。 を定 `catalog::Anchor` 義しない場合、画像の長方形の中心が使用されます(指定と同じ `anchorN=0,0`)。

関連するテキストレイヤーと関 `textPs=` 連するレイヤーは、異なるデ `clipPath=` フォルトのアンカーを持つ場合があります。

## 例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

テンプレートの「例C」を参照して [ください](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)。

## 関連項目 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog::](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) , [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138), [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096), [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)[, Anchor Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
