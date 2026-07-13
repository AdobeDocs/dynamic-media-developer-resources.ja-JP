---
title: opac
description: 不透明度： マテリアルの不透明度を指定します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7acd50b2-5c0c-492e-b5a8-105dc027ebcc
TQID: 'https://experienceleague.adobe.com/j4Y-Lk-BL8VybOYqbP256D81w8FFbQqdS0q8z6Y5l1c'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 70c478ebbe0b38d9e35c1bb26074a458c0197b2b
workflow-type: tm+mt
source-wordcount: 106
ht-degree: 0%

---

# opac{#opac}

不透明度： マテリアルの不透明度を指定します。

` opac= *`val`*`

<table id="simpletable_6AB8CD75F526469FBC9FEAE049792EF2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>材料の不透明度（パーセント）; 0...100 </p> </td> 
 </tr> 
</table>

次のマテリアルとオブジェクトの組み合わせは、不透明度の変数をサポートしています。

* テクスチャの重なりオブジェクトに適用される単色および反復可能なテクスチャ。
* 窓を覆うフレーム オブジェクトに適用される窓を覆うマテリアル。
* テクスチャ オブジェクトまたは壁オブジェクトに適用されるデカール。

素材にアルファチャンネル付きの画像が含まれている場合は、`opac=`を使用して画像の透明度を上げることができますが、不透明度は上がりません。

## プロパティ {#section-352f7b82ede54159b6afb90ae4b559ec}

マテリアル属性： 現在のオブジェクト選択またはマテリアルが不透明度をサポートしていない場合は無視されます。

## 初期設定 {#section-bd45105b1e614f96ad5d521e3ef65736}

`opac=100`、完全に不透明なマテリアルの場合（画像にアルファチャンネルが含まれていない場合）。

