---
description: 不透明度. マテリアルの不透明度を指定します。
seo-description: 不透明度. マテリアルの不透明度を指定します。
seo-title: opac
solution: Experience Manager
title: opac
topic: Scene7 Image Serving - Image Rendering API
uuid: 0f5b11f0-af65-4abd-947e-7a28cb8de263
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# opac{#opac}

不透明度. マテリアルの不透明度を指定します。

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>マテリアルの不透明度(%);0...100 </p> </td> 
 </tr> 
</table>

次のマテリアル/オブジェクトの組み合わせは、可変不透明度をサポートしています。

* テクスチャ可能な重なりオブジェクトに適用されるべた塗りテクスチャと繰り返し可能なテクスチャ。
* 窓カバリングフレームオブジェクトに適用される窓カバリングマテリアル。
* テクスチャ化可能なオブジェクトまたは壁オブジェクトに適用されるデカル。

マテリアルにアルファチャンネルを持つイメージが含まれている場合は、 `opac=` イメージをより透明にし、より不透明にしないようにするために使用できます。

## プロパティ {#section-352f7b82ede54159b6afb90ae4b559ec}

マテリアル属性。 現在のオブジェクト選択またはマテリアルが不透明度をサポートしていない場合は無視されます。

## 初期設定 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`（完全に不透明なマテリアルの場合）。
