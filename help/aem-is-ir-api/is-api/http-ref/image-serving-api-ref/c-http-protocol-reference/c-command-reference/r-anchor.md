---
title: アンカー
description: 画像アンカー。 変換（crop=、scale=、rotate=、flip=）を適用する前に、画像、単色、またはテキスト境界ボックスの長方形のアンカーポイントを定義します。 回転=の回転中心としても機能します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 2%

---

# アンカー{#anchor}

画像アンカー。 変換（crop=、scale=、rotate=、flip=）を適用する前に、画像、単色、またはテキスト境界ボックスの長方形のアンカーポイントを定義します。 回転=の回転中心としても機能します。

`anchor= *`coord`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coord</span> </span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上隅からのピクセルオフセット （int、int） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>ソース イメージの中心からの正規化されたオフセット（実数、実数） </p></td> 
 </tr> 
</table>

アンカーポイントはイメージと一緒に変換され、レイヤーの原点になります（`origin=` も指定されていない場合、`anchor=` は `rotate=` の回転の中心としてのみ使用されます）。

画像アンカー `anchorN=0,0` ソース画像の中央に配置されます。 `anchorN=-0.5,-0.5` または `anchor=0,0` は左上隅にあり、`anchorN=0.5,0.5` はソース画像の右下隅にあります。

## プロパティ {#section-f08942bc6aae46a8b5d341faaff80640}

Source画像属性。 現在の画層、または `layer=comp` の場合は画層 0 に適用されます。

## 初期設定 {#section-35d369fab1254f1a9b91684a6e169ad1}

`anchor=` を指定しない場合は、catalog::Anchor が使用されます。 `catalog::Anchor` が定義されていない場合は、画像の長方形の中心が使用されます（`anchorN=0,0` を指定した場合と同様）。

`textPs=` を含むテキストレイヤーと `clipPath=` を含むレイヤーには、異なるデフォルトのアンカーが存在する場合があります。

## 例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

[ テンプレート ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) の「例 C」を参照してください。

## 関連項目 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog::Anchor](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md)、[origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)、[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)、[clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)、[ テキストレイヤー ](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
