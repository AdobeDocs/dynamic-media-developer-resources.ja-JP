---
description: 不透明度. マテリアルの不透明度を指定します。
solution: Experience Manager
title: opac
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 7910228217db2c97dccd306ce464c69da53ee576
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 3%

---


# opac{#opac}

不透明度. マテリアルの不透明度を指定します。

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>マテリアルの不透明度（パーセント）;0...100 </p> </td> 
 </tr> 
</table>

変数の不透明度は、次のマテリアル/オブジェクトの組み合わせでサポートされています。

* テクスチャの重なり合うオブジェクトに適用されるべた塗りテクスチャと繰り返し可能なテクスチャ。
* 窓カバリングフレームオブジェクトに適用される窓カバリングマテリアル。
* テクスチャオブジェクトまたは壁オブジェクトに適用されるデカル転写。

マテリアルにアルファチャネルのイメージが含まれる場合、`opac=`を使用してイメージを透明にできますが、不透明にはなりません。

## プロパティ {#section-352f7b82ede54159b6afb90ae4b559ec}

マテリアル属性 現在のオブジェクト選択範囲またはマテリアルが不透明度をサポートしていない場合は無視されます。

## 初期設定 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`を指定します。完全に不透明なマテリアルの場合は、チャネルにアルファ画像が含まれていない場合は、このオプションを選択します。
