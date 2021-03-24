---
description: 繰り返し可能なテクスチャには、布地（衣料と表皮の両方）、壁と壁の間の床の覆い、壁紙、カウンタートップ材、木目のテクスチャ、屋根とサイディング材、その他の一般的なテクスチャなど、内部と外部のマテリアルが含まれます。
solution: Experience Manager
title: 繰り返し可能なテクスチャ
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 3%

---


# 繰り返し可能なテクスチャ{#repeatable-textures}

繰り返し可能なテクスチャには、布地（衣料と表皮の両方）、壁と壁の間の床の覆い、壁紙、カウンタートップ材、木目のテクスチャ、屋根とサイディング材、その他の一般的なテクスチャなど、内部と外部のマテリアルが含まれます。

繰り返し可能なテクスチャは、フラット、フローライン、スケッチ、平面、壁、キャビネットの各オブジェクトに適用できます。 テクスチャ不可能なオブジェクトに適用すると、オブジェクトは`color=`（または`color=`が指定されていない場合は`bgc=`）でペイントされます。

イメージを指定する`src=`属性が含まれ、デカールや壁の境界以外のMSSに存在する場合、マテリアルはテクスチャと見なされます。

レンダリング時に、テクスチャマテリアルの`anchor=`点とオブジェクトのテクスチャ接触チャネル点を（ビネットで作成されたとおりに）一致させることで、テクスチャがオブジェクトと位置合わせされます。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src=  </span> </a> </p> </td> 
   <td colname="col2"> <p>反復可能なテクスチャイメージ；required </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res=  </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャ解像度 </p> </td> 
   <td colname="col3"> <span class="codeph"> attribute::Resolution  </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor=  </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャの位置合わせ点 </p> </td> 
   <td colname="col3"> <p>左上隅。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat=  </span> </a> </p> </td> 
   <td colname="col2"> <p>繰り返しモード </p> </td> 
   <td colname="col3"> <p>0（ストレートリピート） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp=  </span> </a> </p> </td> 
   <td colname="col2"> <p>シャープ </p> </td> 
   <td colname="col3"> <p>0（シャープなし） </p> </td> 
  </tr> 
 </tbody> 
</table>

これらの基本アトリビュートに加え、繰り返し可能なテクスチャは、高度なアプリケーションに対して次の特殊用途アトリビュートをサポートしています。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> グラウト=  </span> </a> </p> </td> 
   <td colname="col2"> <p>グラウトの色と太さセラミック/石タイル材料に有用である </p> </td> 
   <td colname="col3"> <p>既にイメージにグラウトが存在します </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align=  </span> </a> </p> </td> 
   <td colname="col2"> <p>整列モード（オブジェクト間）表皮材の用途に使用される </p> </td> 
   <td colname="col3"> <p>中央に一致 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> rotate= </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャの回転角度；壁オブジェクトではサポートされません </p> </td> 
   <td colname="col3"> <p>0（回転なし） </p> </td> 
  </tr> 
 </tbody> 
</table>

