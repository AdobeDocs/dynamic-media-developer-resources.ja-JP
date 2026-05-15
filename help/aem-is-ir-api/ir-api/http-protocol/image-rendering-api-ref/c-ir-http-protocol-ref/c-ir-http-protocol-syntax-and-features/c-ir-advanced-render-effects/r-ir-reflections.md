---
title: リフレクション
description: 周辺光量補正を作成して、ほぼ3Dの反射データを含めることができます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f67ede68-03c0-461f-a16d-a308f76fd24c
TQID: 'https://experienceleague.adobe.com/IzqnNnq7aFgXgEYQ6MJwxqnajYSJlULdEKxaa0OtGWI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 140
ht-degree: 3%

---

# リフレクション{#reflections}

周辺光量補正を作成して、ほぼ3Dの反射データを含めることができます。

作成した場合は、次のマテリアル属性を使用して、マテリアルの反射面プロパティを定義します。

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
   <td> <p><a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca" type="reference" format="dita" scope="local"> <span class="codeph">光沢=</span> </a> </p> </td> 
   <td> <p>表面光沢度 </p> </td> 
   <td> <p>周辺光量補正から </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-glossmap.md#reference-99940148ae6a401482b2d03c68530f3a" type="reference" format="dita" scope="local"> <span class="codeph"> glossmap= </span> </a> </p> </td> 
   <td> <p>光沢のバリエーション（グレースケール画像） </p> </td> 
   <td> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rough.md#reference-00add846b09f4dc39420bda1ca414180" type="reference" format="dita" scope="local"> <span class="codeph"> ラフ= </span> </a> </p> </td> 
   <td> <p>表面粗さ </p> </td> 
   <td> <p>40% </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-type.md#reference-128c7de89e2d46838019b560f3f84a35" type="reference" format="dita" scope="local"> <span class="codeph"> type=</span> </a> </p> </td> 
   <td> <p>マテリアルタイプ </p> </td> 
   <td> <p>0 （不明） </p> </td> 
  </tr> 
 </tbody> 
</table>

レンダラーは、`gloss=`と`rough=`属性の範囲を`type=`に従って調整します。 布地などの一部の材料タイプは、石や金属などの材料タイプよりも反射が少ない場合があります。 さらに、一方に指定した光沢度が同じ場合、もう一方の光沢度とは異なる反射効果が生じることがよくあります。 `type=`が指定されていないか、`0`に設定されている場合、属性`gloss=`と粗さはかなり広い色域になります。

`glossmap=` マテリアルの光沢度をピクセル単位で制御するために使用します。
