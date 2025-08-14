---
title: グラウト
description: グラウトの色と太さをタイル化します。 セラミックと天然石タイルのグラウトをシミュレートします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---

# グラウト {#grout}

グラウトの色と太さをタイル化します。 セラミックと天然石タイルのグラウトをシミュレートします。

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> color </span> </span> </p> </td>
  <td class="stentry"> <p>グラウトの色（グレーまたはRGB）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> width </span> </span> </p> </td>
  <td class="stentry"> <p>グラウトの厚さ。シーンの座標単位（通常はインチ）（実数）。 </p> </td>
 </tr> 
</table>

グラウトの外観を最大限にコントロールするには、次の要件が適用されます。

* タイルは正方形または長方形である必要があります。他の形状は現在サポートされていません。
* 画像には、1 つのタイルのみを含める必要があります。
* イメージ内の既定のグラウト（存在する場合）は、4 つのエッジすべてで同じ厚さにする必要があります。
* 既定のグラウトの厚さは、材料カタログ（`catalog::GroutWidth`）で指定する必要があります。

## プロパティ {#section-de78b678245b4ffda48097c345949e77}

マテリアル アトリビュート。 `*`color`*` RGB カラー値である必要があります。 `*`width`*` は、0 以上の実数値である必要があります。

繰り返し= 4、5、7、8、9、14 以上の場合、または繰り返し可能なテクスチャ以外のマテリアルに指定した場合は無視されます。

## 初期設定 {#section-bfab3621f70b4489a21994ab11b20cc6}

`grout=` が指定されていない場合、画像内のグラウトは変更されません。 `grout= *`color`*` を指定した場合、`*`width`*` のデフォルト値は `catalog::GroutWidth` になります。

## 関連項目 {#section-8d472906a44943f5a8557e98f2fbc71f}

[カラー値](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)
