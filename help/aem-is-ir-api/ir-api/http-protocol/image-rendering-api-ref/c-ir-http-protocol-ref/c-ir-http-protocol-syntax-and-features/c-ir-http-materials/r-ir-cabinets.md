---
title: キャビネット
description: キャビネット マテリアルは、キャビネット スタイル ファイル（.vnc ファイル拡張子）を指定します。このファイルには、キャビネットの写真表現、パラメトリック レイアウト定義、およびキャビネットの前面をレンダリングするために必要なその他の情報が含まれています。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# キャビネット{#cabinets}

キャビネット マテリアルは、キャビネット スタイル ファイル（.vnc ファイル拡張子）を指定します。このファイルには、キャビネットの写真表現、パラメトリック レイアウト定義、およびキャビネットの前面をレンダリングするために必要なその他の情報が含まれています。

[!DNL vnc] ファイルには、繰り返し可能な木目テクスチャを含めるか、テクスチャを `src=` の 2 番目の引数を介して外部に提供できます。 特定の [!DNL vnc] ファイルでは、キャビネットの前面の選択した領域をカラーまたはテクスチャリングできます（通常、ラミネート キャビネット スタイルに使用されます）。

キャビネット マテリアルは、キャビネット オブジェクトにのみ適用できます。

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
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
   <td colname="col2"> <p>キャビネット スタイル ファイル。必須です。 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>オプションのテクスチャ イメージ ファイル（src= </span> の <span class="codeph">2 番目の値）。 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>オプションのテクスチャ解像度。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> 属性：:Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span> </a> </p> </td> 
   <td colname="col2"> <p>キャビネットやテクスチャを色付けします。 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>シャープニング。 </p> </td> 
   <td colname="col3"> <p>0 （シャープなし） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> flags= </span> </a> </p> </td> 
   <td colname="col2"> <p>特別なレンダリングフラグ。 </p> </td> 
   <td colname="col3"> <p>0 （フラグなし） </p> </td> 
  </tr> 
 </tbody> 
</table>
