---
description: 窓カバー材には、ソフトな窓カバー（ドレープ、バランス、カフェカーテン）と、ハードな窓カバー（シェードとブラインド）の両方が含まれます。
solution: Experience Manager
title: 窓の表紙
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: ce6543a1-2438-4661-95bf-ff3d956013bc
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 3%

---

# 窓の表紙{#window-coverings}

窓カバー材には、ソフトな窓カバー（ドレープ、バランス、カフェカーテン）と、ハードな窓カバー（シェードとブラインド）の両方が含まれます。

窓カバーマテリアルは、*窓カバースタイルファイル*（[!DNL .vnw]ファイル拡張子）を指定します。これは、ビネットに似た特殊なデータファイルで、窓カバーを定義するマスク、照明、レイアウト、テクスチャリングデータを含みます。

[!DNL vnw] ファイルには、ウィンドウカバーの色とテクスチャ（ファブリック）は含まれません。この情報は、繰り返し可能なテクスチャと同様に、別々に指定します。

窓カバーマテリアルは、重なり合うオブジェクトである窓カバーフレームオブジェクトにのみ適用できます。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>ウィンドウカバースタイルファイル必須。 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャイメージファイル（<span class="codeph"> src= </span>の2番目の値） </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャの解像度。 </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Resolution  </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat=  </span> </a> </p> </td> 
   <td colname="col2"> <p>繰り返しモード。 </p> </td> 
   <td colname="col3"> <p>0 （ストレートリピート） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color=  </span> </a> </p> </td> 
   <td colname="col2"> <p>べた塗り（またはテクスチャをカラー化）。 </p> </td> 
   <td colname="col3"> <p>128 （ニュートラルグレー） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>シャープ. </p> </td> 
   <td colname="col3"> <p>0（シャープなし） </p> </td> 
  </tr> 
 </tbody> 
</table>
