---
title: ウィンドウのカバー
description: 窓のカバー材には、柔らかい窓のカバー（ドレープ、バランス、カフェカーテン）と硬い窓のカバー（色合いとブラインド）の両方が含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce6543a1-2438-4661-95bf-ff3d956013bc
TQID: 'https://experienceleague.adobe.com/PuQ48u-44qc1KjyuX8HYi5FvCI3UNxsNm-HULPoPhgU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 3%

---

# ウィンドウのカバー{#window-coverings}

窓のカバー材には、柔らかい窓のカバー（ドレープ、バランス、カフェカーテン）と硬い窓のカバー（色合いとブラインド）の両方が含まれます。

窓掛けマテリアルは、*窓掛けスタイルファイル* （[!DNL .vnw] ファイル拡張子）を指定します。これは、周辺光量補正に似た特殊データファイルで、マスク、照明、レイアウト、および窓掛けを定義するテクスチャリングデータを含みます。

[!DNL vnw] ファイルには、ウィンドウのカバーの色とテクスチャ （生地）が含まれていません。 この情報は、繰り返し可能なテクスチャと同様に、個別に指定されます。

窓カバーのマテリアルは、重なり合うオブジェクトであるフレーム オブジェクトをカバーする窓にのみ適用できます。

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
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
   <td colname="col2"> <p>スタイルファイルをカバーするウィンドウ。必須。 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャ画像ファイル （<span class="codeph"> src= </span>の2番目の値）。 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャの解像度： </p> </td> 
   <td colname="col3"> <p> <span class="codeph">属性：：解像度</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>繰り返しモード。 </p> </td> 
   <td colname="col3"> <p>0 （ストレートリピート） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span> </a> </p> </td> 
   <td colname="col2"> <p>べた塗り（またはテクスチャを色付け）。 </p> </td> 
   <td colname="col3"> <p>128 （ニュートラルグレー） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> シャープ= </span> </a> </p> </td> 
   <td colname="col2"> <p>シャープ化： </p> </td> 
   <td colname="col3"> <p>0 （シャープなし） </p> </td> 
  </tr> 
 </tbody> 
</table>
