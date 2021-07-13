---
description: 画像アンカー 変換を適用する前に、画像、べた塗り、またはテキストの境界ボックスの長方形のアンカーポイントを定義します(crop=、scale=、rotate=、flip=)。 また、rotate=の回転の中心としても機能します。
solution: Experience Manager
title: アンカー
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 3%

---

# アンカー{#anchor}

画像アンカー 変換を適用する前に、画像、べた塗り、またはテキストの境界ボックスの長方形のアンカーポイントを定義します(crop=、scale=、rotate=、flip=)。 また、rotate=の回転の中心としても機能します。

`anchor= *`コード`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> コード</span> </span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上隅からのピクセルオフセット（整数、整数） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>ソース画像の中心からの正規化されたオフセット(real、real) </p></td> 
 </tr> 
</table>

アンカーポイントは画像と共に変換され、レイヤーの原点になります（`origin=`も指定されている場合を除き、 `anchor=`は`rotate=`の回転の中心としてのみ使用されます）。

`anchorN=0,0` は、画像アンカーをソース画像の中央に配置します。`anchorN=-0.5,-0.5` また `anchor=0,0` は、が左上隅、 `anchorN=0.5,0.5` がソース画像の右下隅にあります。

## プロパティ {#section-f08942bc6aae46a8b5d341faaff80640}

ソース画像属性。 現在の画層に適用され、 `layer=comp`の場合は画層0に適用されます。

## 初期設定 {#section-35d369fab1254f1a9b91684a6e169ad1}

`anchor=`を指定しない場合は、catalog::Anchorが使用されます。 `catalog::Anchor`を定義しない場合は、画像の長方形の中心が使用されます（`anchorN=0,0`を指定する場合と同じ）。

`textPs=`が含まれるテキストレイヤーと、`clipPath=`が含まれるレイヤーは、異なるデフォルトアンカーを持つ場合があります。

## 例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の「Example C」を参照してください。

## 関連項目 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog::Anchor](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) 、 [origin=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)、 [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)、 [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)、 [Text Layers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
