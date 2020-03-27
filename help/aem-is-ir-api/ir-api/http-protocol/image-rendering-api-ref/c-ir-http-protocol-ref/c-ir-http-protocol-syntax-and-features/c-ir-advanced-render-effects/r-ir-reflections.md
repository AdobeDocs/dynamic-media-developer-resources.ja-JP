---
description: ビネットは、3Dに近い反射データを含むようにオーサリングできます。
seo-description: ビネットは、3Dに近い反射データを含むようにオーサリングできます。
seo-title: 反射
solution: Experience Manager
title: 反射
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d86f566-0f02-4304-8a6c-08b1a2e9c72e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 反射{#reflections}

ビネットは、3Dに近い反射データを含むようにオーサリングできます。

オーサリングされている場合は、次のマテリアル属性を使用してマテリアルの反射サーフェスプロパティが定義されます。

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
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph"> gloss=</span></a> </p> </td> 
   <td> <p>表面光沢度 </p> </td> 
   <td> <p>ビネットから </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span></a> </p> </td> 
   <td> <p>光沢のバリエーション（グレースケール画像） </p> </td> 
   <td> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> 粗= </span></a> </p> </td> 
   <td> <p>表面粗さ </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>マテリアルタイプ </p> </td> 
   <td> <p>0（不明） </p> </td> 
  </tr> 
 </tbody> 
</table>

レンダラーは、に従ってと属性の `gloss=` 範囲 `rough=` を調整しま `type=`す。 布地などの材料の種類によっては、通常、石や金属などの材料の種類よりも反射率が低く、一方に同じ光沢度を指定すると、他方とは異なる反射効果が得られます。 `gloss=`を指定しない場合、または0に設定した場合、粗さ `type=` はかなり広い色域を持ちます。

`glossmap=` は、ピクセル単位でマテリアルの光沢度を制御するのに使用できます。
