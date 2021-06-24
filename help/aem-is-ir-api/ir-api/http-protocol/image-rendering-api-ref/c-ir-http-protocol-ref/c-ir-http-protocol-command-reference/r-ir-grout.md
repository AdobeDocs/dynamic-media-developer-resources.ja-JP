---
description: タイルグラウトの色と厚さ。 セラミックや天然石タイルのグラウトをシミュレートします。
solution: Experience Manager
title: グラウト
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 2%

---

# グラウト{#grout}

タイルグラウトの色と厚さ。 セラミックや天然石タイルのグラウトをシミュレートします。

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color  </span> </span> </p> </td> 
  <td class="stentry"> <p>グラウトの色（グレーまたはRGB）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td> 
  <td class="stentry"> <p>グラウトの厚さ；シーンの座標単位（通常はインチ）（実数） </p> </td> 
 </tr> 
</table>

グラウトの外観を最大限に制御するには、次の要件が適用されます。

* タイルは四角または長方形でなければなりません。現時点では、他の図形はサポートされていません。
* 画像には、1つのタイルのみを含める必要があります。
* イメージ内の既定のグラウト（存在する場合）は、4つのエッジすべてで同じ厚さにする必要があります。
* 既定のグラウトの厚さは、マテリアルカタログ( `catalog::GroutWidth` )で指定する必要があります。

## プロパティ {#section-de78b678245b4ffda48097c345949e77}

マテリアル属性。 `*``*` colorは、RGBカラー値である必要があります。`*``*` widthは、0以上の実数にする必要があります。

繰り返し= 4、5、7、8、9、14以上の場合や、繰り返し可能なテクスチャ以外のマテリアルに対して指定した場合は無視されます。

## 初期設定 {#section-bfab3621f70b4489a21994ab11b20cc6}

`grout=`を指定しない場合、イメージのグラウトは変更されません。 ` grout= *`color`*`を指定した場合、`*`width`*`はデフォルトで`catalog::GroutWidth`になります。

## 関連項目 {#section-8d472906a44943f5a8557e98f2fbc71f}

[カラー値](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
