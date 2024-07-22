---
title: 反射
description: ビネットを作成して、3D に近い反射データを含めることができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---

# 反射{#reflections}

ビネットを作成して、3D に近い反射データを含めることができます。

作成した場合、次のマテリアル属性を使用してマテリアルの反射サーフェス プロパティを定義します。

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
   <td> <p>ビネットから </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span> </a> </p> </td> 
   <td> <p>グロスバリエーション（グレースケール画像） </p> </td> 
   <td> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> rough= </span> </a> </p> </td> 
   <td> <p>表面粗さ </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>材料タイプ </p> </td> 
   <td> <p>0 （不明） </p> </td> 
  </tr> 
 </tbody> 
</table>

レンダラーは、`type=` に従って `gloss=` と `rough=` 属性の範囲を調整します。 布地などの一部のマテリアル タイプは、石や金属などのマテリアル タイプよりも反射が少なくなります。 また、一方に指定した量の光沢は、他方とは異なる反射効果を生じることがよくあります。 属性 `gloss=` と粗さは、`type=` が指定されていないか、または `0` に設定されている場合、かなり広い色域を持ちます。

`glossmap=` マテリアルの光沢をピクセル単位でコントロールするために使用します。
