---
title: キャビネット
description: キャビネットのマテリアルは、キャビネットのスタイル ファイル（.vnc ファイル拡張子）を指定します。キャビネットの写真表現と、パラメトリック レイアウト定義およびその他のキャビネット フロントのレンダリングに必要な情報を含む特殊なデータ ファイルです。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
TQID: 'https://experienceleague.adobe.com/SzkFcvt2K-pHseOvk42kwWVaIl2-BnQK8aSEwSTB9zA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 4339f336345d7d7f3c05c7f5a18fbd28bcfd382b
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 3%

---

# キャビネット{#cabinets}

キャビネットのマテリアルは、キャビネットのスタイル ファイル（.vnc ファイル拡張子）を指定します。キャビネットの写真表現と、パラメトリック レイアウト定義およびその他のキャビネット フロントのレンダリングに必要な情報を含む特殊なデータ ファイルです。

[!DNL vnc] ファイルには、繰り返し可能な木目のテクスチャを含めるか、または`src=`への2番目の引数を使用して外部からテクスチャを提供できます。 特定の[!DNL vnc] ファイルでは、キャビネット フロントの選択した領域にカラーを適用したり、テクスチャを適用したりできます（通常はラミネート キャビネット スタイルに使用されます）。

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
   <td colname="col2"> <p>キャビネットスタイルファイル。必須。 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>オプションのテクスチャ画像ファイル （<span class="codeph"> src= </span>の2番目の値）。 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>オプションのテクスチャ解像度。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph">属性：：解像度</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span> </a> </p> </td> 
   <td colname="col2"> <p>キャビネットやテクスチャをカラー化します。 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> シャープ= </span> </a> </p> </td> 
   <td colname="col2"> <p>シャープ化： </p> </td> 
   <td colname="col3"> <p>0 （シャープなし） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> フラグ= </span> </a> </p> </td> 
   <td colname="col2"> <p>特殊レンダリングフラグ。 </p> </td> 
   <td colname="col3"> <p>0 （フラグなし） </p> </td> 
  </tr> 
 </tbody> 
</table>

