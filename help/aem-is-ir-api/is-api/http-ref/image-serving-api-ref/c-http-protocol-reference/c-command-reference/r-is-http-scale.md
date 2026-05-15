---
title: 拡大・縮小
description: 画像を拡大・縮小。 レイヤーのソース画像を、フル解像度の画像に対して係数ごとに拡大・縮小します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
TQID: 'https://experienceleague.adobe.com/qC-yBofpV9CNTTjb8Ll1EYV6Q1YA0BUsLLEHadfLAu8'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 113
ht-degree: 2%

---

# 拡大・縮小{#scale}

画像を拡大・縮小。 レイヤーのソース画像を、フル解像度の画像に対して係数ごとに拡大・縮小します。

`scale= *`係数`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">要素</span> </p> </td> 
  <td class="stentry"> <p>スケール係数（実数、0.0より大きい）。 </p></td> 
 </tr> 
</table>

`scale=1`の場合、拡大・縮小は適用されません。 ダウンスケールが1.0より小さく、1.0より大きい&#x200B;*`factor`*&#x200B;は、ソース画像を拡大します。

## プロパティ {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Source image/mask属性。 現在のレイヤーにも`size=`が指定されている場合は無視されます。 `res=`を上書きします。 `layer=comp`に指定されている場合は、レイヤー0に適用されます。 レイヤーが画像またはマスクに関連付けられていない場合は無視されます。

## 初期設定 {#section-26e64904362342a5a62c5f6598f330c4}

指定しない場合は、`res=`が使用されます。 `res=`が指定されていない場合、画像は拡大・縮小せずに使用されます。

## 関連項目 {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55)、[size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
