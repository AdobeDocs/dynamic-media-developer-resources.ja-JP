---
title: デカール
description: デカールの素材には、アップリケ、T シャツのプリント、刺繍や印刷されたロゴなどのアパレル構成が含まれます。 また、エリア敷物、壁掛けアート、標識など、屋内または屋外の用途で使用される繰り返し不可能な平らなオブジェクトも含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 07190abd-9f6f-46b5-bf77-cd97c48fc9be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 1%

---

# デカール{#decals}

デカールの素材には、アップリケ、T シャツのプリント、刺繍や印刷されたロゴなどのアパレル構成が含まれます。 また、エリア敷物、壁掛けアート、標識など、屋内または屋外の用途で使用される繰り返し不可能な平らなオブジェクトも含まれます。

デカル MSS で指定されているマテリアルは、デカル転写と見なされます。 通常、デカルは RGBA 画像で、アルファ チャンネルによってデカルのシェイプが定義されます。

各フラット オブジェクト、フローライン オブジェクト、スケッチ オブジェクト、平面オブジェクト、または壁オブジェクトに 1 つのデカル転写を適用できます（[ テクスチャなし ] フラグが設定されている場合を除く）。 デカル転写は、デカル転写の `anchor=` をビネット オブジェクトのデカル転写の原点に位置合わせすることによって、オブジェクトに適用されます。 位置は `pos=` でさらに調整できます。

デカール マテリアルで厚みが定義され、ビネット オブジェクトでライト ベクトルが定義されている場合、ドロップ シャドウがレンダリングされます。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> size= </span> </a> </p> </td> 
   <td colname="col2"> <p>デカールの幅、高さ、および厚さ（ドロップシャドウの場合）。 </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x <span class="codeph"> res </span>, <span class="varname"> imageHeight </span> x <span class="codeph"> res, 0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャの解像度（size=が指定されている場合は無視されます）。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 属性：:Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span> </a> </p> </td> 
   <td colname="col2"> <p>デカル転写の位置合わせポイント。 </p> </td> 
   <td colname="col3"> <p>画像センター </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span> </a> </p> </td> 
   <td colname="col2"> <p>デカル転写の相対位置。 </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span> </a> </p> </td> 
   <td colname="col2"> <p>デカル転写の不透明度 </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </td> 
   <td colname="col2"> <p>シャープニング。 </p> </td> 
   <td colname="col3"> <p>0 （シャープなし） </p> </td> 
  </tr> 
 </tbody> 
</table>
