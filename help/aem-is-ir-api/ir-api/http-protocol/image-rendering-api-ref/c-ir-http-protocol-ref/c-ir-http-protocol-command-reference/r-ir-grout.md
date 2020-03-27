---
description: 目地の色と太さを並べます。 セラミックや天然の石タイルのグラウトをシミュレートします。
seo-description: 目地の色と太さを並べます。 セラミックや天然の石タイルのグラウトをシミュレートします。
seo-title: グラウト
solution: Experience Manager
title: グラウト
topic: Scene7 Image Serving - Image Rendering API
uuid: 00069004-40f2-4ab6-85d8-ca197b7bef69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# グラウト{#grout}

目地の色と太さを並べます。 セラミックや天然の石タイルのグラウトをシミュレートします。

grout= *`color`*[、*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 色 </span></span> </p> </td> 
  <td class="stentry"> <p>グラウトの色（グレーまたはRGB） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>グラウトの厚さ；シーンの座標単位（通常はインチ）（実数）。 </p> </td> 
 </tr> 
</table>

グラウトの外観を最大限に制御するため、次の要件が適用されます。

* タイルは正方形または長方形でなければなりません。現時点では、他の図形はサポートされていません。
* 画像には、1つのタイルのみを含める必要があります。
* イメージ内の既定のグラウト（存在する場合）は、4つのエッジすべてに同じ厚さを持つ必要があります。
* 既定のグラウトの厚さは、材料カタログ( `catalog::GroutWidth`)で指定する必要があります。

## プロパティ {#section-de78b678245b4ffda48097c345949e77}

マテリアル属性。 ` *`colorは`*` RGBカラー値である必要があります。 ` *`widthは`*` 、0以上の実数である必要があります。

repeat = 4、5、7、8、9、14以上の場合、または繰り返しテクスチャ以外のマテリアルに対して指定した場合は無視されます。

## 初期設定 {#section-bfab3621f70b4489a21994ab11b20cc6}

を指定 `grout=` しない場合、画像内のグラウトは変更されません。 colorを指 ` grout= *`定した場`*` 合、widthのデフ ` *`ォルト値は`*``catalog::GroutWidth`です。

## 関連項目 {#section-8d472906a44943f5a8557e98f2fbc71f}

[カラー値](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
