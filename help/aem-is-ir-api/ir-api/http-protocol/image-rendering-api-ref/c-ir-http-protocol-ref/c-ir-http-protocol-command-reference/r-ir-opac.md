---
description: 不透明度. マテリアルの不透明度を指定します。
solution: Experience Manager
title: opac
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 3%

---

# opac{#opac}

不透明度. マテリアルの不透明度を指定します。

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>マテリアルの不透明度（パーセント）0...100 </p> </td> 
 </tr> 
</table>

次のマテリアル/オブジェクトの組み合わせは、変数の不透明度をサポートしています。

* テクスチャの重なり合うオブジェクトに適用された、べた塗りのテクスチャと繰り返し可能なテクスチャ。
* 窓カバーフレームオブジェクトに適用される窓カバーマテリアル。
* テクスチャオブジェクトまたは壁オブジェクトに適用されるデカール。

アルファチャンネルを持つイメージがマテリアルに含まれている場合、 `opac=`を使用してイメージを透明にできますが、不透明にすることはできません。

## プロパティ {#section-352f7b82ede54159b6afb90ae4b559ec}

マテリアル属性。 現在のオブジェクト選択またはマテリアルが不透明度をサポートしていない場合は無視されます。

## 初期設定 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`：完全に不透明なマテリアル（イメージにアルファチャンネルが含まれていない場合）。
