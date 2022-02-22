---
title: opac
description: 不透明度. マテリアルの不透明度を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 3%

---

# opac{#opac}

不透明度. マテリアルの不透明度を指定します。

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>マテリアルの不透明度（パーセント）0...100 </p> </td> 
 </tr> 
</table>

次のマテリアル/オブジェクトの組み合わせは、変数の不透明度をサポートしています。

* テクスチャの重なりオブジェクトに適用された、べた塗りのテクスチャと繰り返し可能なテクスチャ。
* 窓被覆フレームオブジェクトに適用される窓被覆マテリアル。
* テクスチャオブジェクトまたは壁オブジェクトに適用されるデカール。

マテリアルにアルファチャンネルを持つ画像が含まれる場合、 `opac=` を使用すると、画像がより透明になりますが、より不透明になりません。

## プロパティ {#section-352f7b82ede54159b6afb90ae4b559ec}

材料属性。 現在のオブジェクト選択またはマテリアルが不透明度をサポートしていない場合は無視されます。

## 初期設定 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`：完全に不透明なマテリアル（画像にアルファチャンネルが含まれていない場合）。
