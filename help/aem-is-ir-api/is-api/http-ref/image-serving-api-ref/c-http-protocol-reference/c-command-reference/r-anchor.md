---
title: アンカー
description: 画像アンカー： 変形（crop=、scale=、rotate=、flip=）を適用する前に、画像、単色、またはテキストのバウンディングボックスの長方形のアンカーポイントを定義します。 rotate=の回転の中心としても機能します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f62ae048-0dcc-4e93-a9f1-2e4db6bef51f
TQID: 'https://experienceleague.adobe.com/GKa8ChLxu85Wmi65uak7Kqn-Kme1GXL0FToaMAgHKoA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 218
ht-degree: 2%

---

# アンカー{#anchor}

画像アンカー： 変形（crop=、scale=、rotate=、flip=）を適用する前に、画像、単色、またはテキストのバウンディングボックスの長方形のアンカーポイントを定義します。 rotate=の回転の中心としても機能します。

`anchor= *` コード `*`

`anchorN= *`coordN`*`

<table id="simpletable_3ED1CD0BF473439FA1132FC84B4452A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> コード </span> </span> </p> </td> 
  <td class="stentry"> <p>ソースイメージの左上隅からのピクセルオフセット（int、int） </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p>ソース画像の中心からの正規化されたオフセット（実数、実数） </p></td> 
 </tr> 
</table>

アンカーポイントは画像で変形され、レイヤーの起点になります（`origin=`が指定されている場合を除く。この場合、`anchor=`は`rotate=`の回転中心としてのみ使用されます）。

`anchorN=0,0`は、画像アンカーをソース画像の中央に配置します。 `anchorN=-0.5,-0.5`または`anchor=0,0`は左上隅にあり、`anchorN=0.5,0.5`はソース画像の右下隅にあります。

## プロパティ {#section-f08942bc6aae46a8b5d341faaff80640}

Source画像属性。 現在のレイヤーまたは`layer=comp`の場合はレイヤー0に適用されます。

## 初期設定 {#section-35d369fab1254f1a9b91684a6e169ad1}

`anchor=`が指定されていない場合は、catalog::Anchorが使用されます。 `catalog::Anchor`が定義されていない場合、画像の長方形の中心が使用されます（`anchorN=0,0`を指定することと同じです）。

`textPs=`を含むテキストレイヤーと`clipPath=`を含むレイヤーでは、デフォルトアンカーが異なる場合があります。

## 例 {#section-cc127e6b1ea94524900b5c0dd8b4c7ec}

[&#x200B; テンプレート &#x200B;](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e)の「Cの例」を参照してください。

## 関連項目 {#section-9877ea3a0743492aaa4fa1dfc9510b07}

[&#x200B; カタログ：：アンカー](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-anchor-cat.md)、[&#x200B; オリジン=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-origin.md#reference-e11c7ac06e2240cc884c3fec98f05138)、[回転=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)、[&#x200B; クリップパス=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d)、[&#x200B; テキストレイヤー](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
