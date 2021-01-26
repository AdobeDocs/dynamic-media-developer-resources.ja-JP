---
description: 画像アンカー 変換(crop=、scale=、rotate=、flip=)を適用する前に、画像、べた塗り色またはテキストバウンディングボックスの長方形のアンカーポイントを定義します。 また、rotate=の回転の中心としての役割も果たします。
seo-description: 画像アンカー 変換(crop=、scale=、rotate=、flip=)を適用する前に、画像、べた塗り色またはテキストバウンディングボックスの長方形のアンカーポイントを定義します。 また、rotate=の回転の中心としての役割も果たします。
seo-title: アンカー
solution: Experience Manager
title: アンカー
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 3b174360-9bb7-4dc8-83be-6b8c4ea88cd4
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 3%

---


# アンカー{#anchor}

画像アンカー 変換(crop=、scale=、rotate=、flip=)を適用する前に、画像、べた塗り色またはテキストバウンディングボックスの長方形のアンカーポイントを定義します。 また、rotate=の回転の中心としての役割も果たします。

`anchor= *`共謀者`*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 共謀者</span> </span> </p> </td> 
  <td class="stentry"> <p>ソース画像の左上隅からのピクセルオフセット(int、int) </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>ソース画像の中心からの正規化オフセット(real、real) </p></td> 
 </tr> 
</table>

アンカーポイントは画像を使用して変換され、レイヤーの接触チャネルポイントになります（`origin=`も指定する場合を除き、`anchor=`は`rotate=`の回転の中心としてのみ使用されます）。

`anchorN=0,0` ソース画像の中央に画像アンカーを配置します。`anchorN=-0.5,-0.5` または、 `anchor=0,0` が左上隅で、 `anchorN=0.5,0.5` がソース画像の右下隅にあります。

## プロパティ {#section-f08942bc6aae46a8b5d341faaff80640}

ソース画像属性。 現在の画層に適用されます。`layer=comp`の場合は画層0に適用されます。

## 初期設定 {#section-35d369fab1254f1a9b91684a6e169ad1}

`anchor=`を指定しない場合は、catalog::Anchorが使用されます。 `catalog::Anchor`を定義しない場合は、画像の長方形の中心が使用されます（`anchorN=0,0`を指定する場合と同じ）。

`textPs=`に関係するテキストレイヤーと`clipPath=`に関係するレイヤーは、異なるデフォルトアンカーを持つ場合があります。

## 例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

[テンプレート](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の「例C」を参照してください。

## 関連項目 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[catalog::](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md) ,  [接触チャネル=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138),  [rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d) [, anchor textLayers](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
