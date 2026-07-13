---
title: デカール
description: デカール素材には、アップリケ、T シャツプリント、刺繍または印刷されたロゴなどのアパレル作品が含まれます。 また、エリアラグ、壁掛けアート、看板など、内部または外部のアプリケーションで使用される繰り返し不可能な平らなオブジェクトも含まれています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 07190abd-9f6f-46b5-bf77-cd97c48fc9be
TQID: 'https://experienceleague.adobe.com/fjh30cRKJYFE2ZAi7PV0g017dzYu1tjXWMZyp-DUSDI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 231
ht-degree: 3%

---

# デカール{#decals}

デカール素材には、アップリケ、T シャツプリント、刺繍または印刷されたロゴなどのアパレル作品が含まれます。 また、エリアラグ、壁掛けアート、看板など、内部または外部のアプリケーションで使用される繰り返し不可能な平らなオブジェクトも含まれています。

マテリアルがデカール MSSで指定されている場合、そのマテリアルはデカールと見なされます。 デカールは通常、RGBA画像で、アルファチャンネルがデカールの形状を定義します。

デカールは、フラット、フローライン、スケッチ、平面、または壁の各オブジェクトに1つずつ適用できます（「テクスチャなし」フラグが設定されている場合を除く）。 デカールの`anchor=`をビネット オブジェクトのデカールの原点に合わせることで、デカールがオブジェクトに適用されます。 位置は`pos=`でさらに調整できます。

デカール マテリアルが厚みを定義し、周辺光量補正オブジェクトが光ベクトルを定義する場合、ドロップシャドウがレンダリングされます。

<table id="table_3F119BC9B7654FD092826A34F5827268"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
   <th colname="col3" class="entry"> <p>初期設定 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>画像（通常はアルファ付き）。必須。 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> サイズ= </span> </a> </p> </td> 
   <td colname="col2"> <p>デカールの幅、高さ、厚さ（ドロップシャドウ用）。 </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph"> res </span>, <span class="varname"> imageHeight </span> x <span class="codeph"> res, 0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャの解像度（size=が指定されている場合は無視）。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph">属性：：解像度</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> アンカー= </span> </a> </p> </td> 
   <td colname="col2"> <p>デカール整列ポイント。 </p> </td> 
   <td colname="col3"> <p>画像センター： </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span> </a> </p> </td> 
   <td colname="col2"> <p>相対的なデカール位置： </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span> </a> </p> </td> 
   <td colname="col2"> <p>デカールの不透明度： </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> シャープ= </span> </a> </td> 
   <td colname="col2"> <p>シャープ化： </p> </td> 
   <td colname="col3"> <p>0 （シャープなし） </p> </td> 
  </tr> 
 </tbody> 
</table>

