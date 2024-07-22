---
title: opac
description: 不透明度。 マテリアルの不透明度を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 0%

---

# opac{#opac}

不透明度。 マテリアルの不透明度を指定します。

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>マテリアルの不透明度（パーセント）、0...100 </p> </td> 
 </tr> 
</table>

次のマテリアルとオブジェクトの組み合わせは、不透明度の可変をサポートします。

* テクスチャのオーバーラップ オブジェクトに適用される単色および繰り返し可能なテクスチャ
* 窓覆いフレーム オブジェクトに適用される窓覆いマテリアル。
* テクスチャ オブジェクトまたは壁オブジェクトに適用されるデカル転写

マテリアルにアルファ チャンネルを持つイメージが含まれ `opac=` いる場合は、イメージをより不透明にすることはできませんが、不透明にすることはできます。

## プロパティ {#section-352f7b82ede54159b6afb90ae4b559ec}

マテリアル アトリビュート。 現在のオブジェクト選択またはマテリアルが不透明度をサポートしていない場合は無視されます。

## 初期設定 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`：完全に不透明なマテリアル（イメージにアルファ チャンネルが含まれていない場合）。
