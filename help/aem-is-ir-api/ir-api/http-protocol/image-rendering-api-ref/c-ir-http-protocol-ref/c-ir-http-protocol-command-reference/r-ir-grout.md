---
title: グラウト
description: タイルグラウトの色と太さ。 セラミックと天然石タイルのグラウトをシミュレートします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 6647b459-11d2-47e4-9033-3a740f01a623
TQID: 'https://experienceleague.adobe.com/FrYxcizVu3nXej1tt4QpX0AsLEylXTfwYRaSQP43HNI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 1%

---

# グラウト {#grout}

タイルグラウトの色と太さ。 セラミックと天然石タイルのグラウトをシミュレートします。

grout= *`color`*[,*`width`*]

<table id="simpletable_302B78CFC8F14E0F962D1D2064AD1371"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> カラー</span> </span> </p> </td>
  <td class="stentry"> <p>グラウトカラー（グレーまたはRGB）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname">幅</span> </span> </p> </td>
  <td class="stentry"> <p>グラウトの厚さ。シーンの座標単位（通常はインチ）（実数）。 </p> </td>
 </tr> 
</table>

グラウトの外観を最大限に制御するには、次の要件が適用されます。

* タイルは正方形または長方形にする必要があります。現在、他のシェイプはサポートされていません。
* 画像には、1つのタイルのみを含める必要があります。
* 画像内のデフォルトのグラウト（ある場合）は、4つのエッジすべてで同じ厚みにする必要があります。
* 既定のグラウトの厚みは、材料カタログ （`catalog::GroutWidth`）で指定する必要があります。

## プロパティ {#section-de78b678245b4ffda48097c345949e77}

マテリアル属性： `*`color`*`はRGB カラー値である必要があります。 `*`width`*`は実数値0以上である必要があります。

繰り返し= 4、5、7、8、9、14以上の場合、または繰り返し可能なテクスチャ以外のマテリアルに指定された場合は無視されます。

## 初期設定 {#section-bfab3621f70b4489a21994ab11b20cc6}

`grout=`が指定されていない場合、画像内のグラウトは変更されません。 `grout= *`color`*`が指定されている場合、`*`width`*`はデフォルトで`catalog::GroutWidth`になります。

## 関連項目 {#section-8d472906a44943f5a8557e98f2fbc71f}

[カラー値](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/r-ir-color-values.md#reference-657f95c0841742d2a55a48bc938303f6)

