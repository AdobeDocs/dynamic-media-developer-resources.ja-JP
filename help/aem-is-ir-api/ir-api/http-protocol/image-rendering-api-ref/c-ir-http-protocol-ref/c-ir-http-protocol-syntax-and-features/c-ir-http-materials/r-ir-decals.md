---
description: デカルのマテリアルには、アプリケ、Tシャツ、刺繍や印刷ロゴなどのアパレル構成要素、エリアラグ、壁掛けアート、看板などの内装や外装に使用される繰り返し不可能なフラットオブジェクトが含まれます。
seo-description: デカルのマテリアルには、アプリケ、Tシャツ、刺繍や印刷ロゴなどのアパレル構成要素、エリアラグ、壁掛けアート、看板などの内装や外装に使用される繰り返し不可能なフラットオブジェクトが含まれます。
seo-title: デカル
solution: Experience Manager
title: デカル
topic: Scene7 Image Serving - Image Rendering API
uuid: 6e64f382-f15f-4018-b00c-4fd21a4ebc8c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# デカル{#decals}

デカルのマテリアルには、アプリケ、Tシャツ、刺繍や印刷ロゴなどのアパレル構成要素、エリアラグ、壁掛けアート、看板などの内装や外装に使用される繰り返し不可能なフラットオブジェクトが含まれます。

デカルMSSで指定されている場合、マテリアルはデカルと見なされます。 デカルは通常、デカルの形状を定義するアルファチャンネルを持つRGBAイメージです。

デカル転写は、フラット、フローライン、スケッチ、平面、または壁の各オブジェクトに1つずつ適用できます（[テクスチャなし]フラグが設定されていない場合）。 デカル転写の原点をビネットオブジェクトのデカル原点に合わせ `anchor=` て、デカル転写をオブジェクトに適用します。 位置は、を使用してさらに調整できま `pos=`す。

デカールマテリアルで厚みを定義し、ビネットオブジェクトでライトベクトルを定義する場合、ドロップシャドウがレンダリングされます。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>画像（通常はアルファ付き）必須。 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-size.md#reference-1220d6fbcde4479aba91de7adacdc988" type="reference" format="dita" scope="local"> <span class="codeph"> サイズ= </span></a> </p> </td> 
   <td colname="col2"> <p>デカル転写の幅、高さ、厚さ（ドロップシャドウの場合）。 </p> </td> 
   <td colname="col3"> <p> <span class="varname"> imageWidth </span> x res、imageHeight <span class="codeph"> x </span><span class="varname"></span><span class="codeph"> res、0 </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>テクスチャの解像度（size=が指定されている場合は無視） </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span></a> </p> </td> 
   <td colname="col2"> <p>デカルの位置合わせ点 </p> </td> 
   <td colname="col3"> <p>画像センター </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-pos.md#reference-22c10904a0ce4c8bb41c2c78104221b8" type="reference" format="dita" scope="local"> <span class="codeph"> pos= </span></a> </p> </td> 
   <td colname="col2"> <p>相対的なデカール位置 </p> </td> 
   <td colname="col3"> <p>0, 0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-opac.md#reference-136b8563da714313a9e103f4ce179c5b" type="reference" format="dita" scope="local"> <span class="codeph"> opac= </span></a> </p> </td> 
   <td colname="col2"> <p>デカールの不透明度 </p> </td> 
   <td colname="col3"> <p>100% </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span></a> </td> 
   <td colname="col2"> <p>シャープ. </p> </td> 
   <td colname="col3"> <p>0（シャープなし） </p> </td> 
  </tr> 
 </tbody> 
</table>

