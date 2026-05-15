---
title: 反復可能なテクスチャ
description: 繰り返し可能なテクスチャには、生地（アパレルと室内装飾品の両方）、壁から壁までの床のカバー、壁紙、カウンタートップ素材、木目のテクスチャ、屋根とサイディング素材、その他の一般的なテクスチャなどの内部および外部素材が含まれます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
TQID: 'https://experienceleague.adobe.com/hWfVo7g-LL9l-G8FkN4HZ4B1X7uX85LlklZFjNBsjZI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 251
ht-degree: 3%

---

# 反復可能なテクスチャ{#repeatable-textures}

繰り返し可能なテクスチャには、生地（アパレルと室内装飾品の両方）、壁から壁までの床のカバー、壁紙、カウンタートップ素材、木目のテクスチャ、屋根とサイディング素材、その他の一般的なテクスチャなどの内部および外部素材が含まれます。

繰り返し可能なテクスチャは、フラット、フローライン、スケッチ、平面、壁、キャビネット オブジェクトに適用できます。 テクスチャリングできないオブジェクトに適用すると、オブジェクトは`color=` （`color=`が指定されていない場合は`bgc=`）でペイントされます。

マテリアルに画像を指定する`src=`属性が含まれている場合や、デカールや壁の境界以外のMSSでマテリアルが発生する場合、そのマテリアルはテクスチャと見なされます。

レンダリング時に、テクスチャ マテリアルの`anchor=`点とオブジェクトのテクスチャ起点（周辺光量補正で作成されたもの）を一致させることで、テクスチャがオブジェクトに整列されます。

<table id="table_992A6E93E4274B598A236F8F728F017A"> 
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
   <td colname="col2"> <p>繰り返し可能なテクスチャ画像。必須 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャ解像度 </p> </td> 
   <td colname="col3"> <span class="codeph">属性：：解像度</span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> アンカー= </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャの整列ポイント </p> </td> 
   <td colname="col3"> <p>左上隅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>リピートモード </p> </td> 
   <td colname="col3"> <p>0 （ストレートリピート）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> シャープ= </span> </a> </p> </td> 
   <td colname="col2"> <p>シャープ </p> </td> 
   <td colname="col3"> <p>0 （シャープなし）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

これらの基本属性に加えて、繰り返し可能なテクスチャでは、高度なアプリケーションに対して次の特殊目的の属性をサポートしています。

<table id="table_A97365804CB143DEB31F26A65DA3CE04"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>属性 </p> </th> 
   <th colname="col2" class="entry"> <p>説明 </p> </th> 
   <th colname="col3" class="entry"> <p>初期設定 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> グラウト= </span> </a> </p> </td> 
   <td colname="col2"> <p>グラウト色と厚さ；有用なためセラミック/石タイル材料 </p> </td> 
   <td colname="col3"> <p>グラウトはすでに画像内に存在します </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph">の整列= </span> </a> </p> </td> 
   <td colname="col2"> <p>整列モード（オブジェクト間）。室内装飾品アプリケーションに使用されます。 </p> </td> 
   <td colname="col3"> <p>Center-matched </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph">回転= </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャの回転角度。壁オブジェクトではサポートされていません </p> </td> 
   <td colname="col3"> <p>0 （回転なし） </p> </td> 
  </tr> 
 </tbody> 
</table>
