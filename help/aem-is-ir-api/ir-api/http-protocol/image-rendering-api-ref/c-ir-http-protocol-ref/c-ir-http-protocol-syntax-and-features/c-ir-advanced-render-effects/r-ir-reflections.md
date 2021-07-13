---
description: ビネットは、3Dに近い反射データを含むように作成できます。
solution: Experience Manager
title: 反射
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 4%

---

# 反射{#reflections}

ビネットは、3Dに近い反射データを含むように作成できます。

オーサリングした場合は、次のマテリアル属性を使用して、マテリアルの反射サーフェスプロパティを定義します。

<table id="table_8769C726A17E412FB41F7CB87690B1FE"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>属性 </p> </th> 
   <th class="entry"> <p>説明 </p> </th> 
   <th class="entry"> <p>初期設定 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> gloss=</span> </a> </p> </td> 
   <td> <p>サーフェス光沢 </p> </td> 
   <td> <p>vignetteから </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap=  </span> </a> </p> </td> 
   <td> <p>光沢の変化（グレースケール画像） </p> </td> 
   <td> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> rough=  </span> </a> </p> </td> 
   <td> <p>表面粗さ </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>材料の種類 </p> </td> 
   <td> <p>0 （不明） </p> </td> 
  </tr> 
 </tbody> 
</table>

レンダラーは`gloss=`属性と`rough=`属性の範囲を`type=`に従って調整します。 生地などの材料の種類には、石や金属などの材料の種類と比べて反射が少ないものもあり、一方に指定した光沢の量が同じで、他方とは反射効果が異なる場合があります。 `gloss=`粗さは、が指定されていない場合や0に設定され `type=` ている場合、かなり広い色域を持ちます。

`glossmap=` は、ピクセル単位でマテリアルの光沢度を制御するために使用できます。
