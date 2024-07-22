---
title: 反復可能なテクスチャ
description: 繰り返し可能なテクスチャには、内装材および外装材（布地、アパレルおよび室内装飾材の両方）、壁から壁までの床材、壁紙、カウンタートップ材、木目調、屋根およびサイディング材などの一般的なテクスチャなどがあります。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3693498b-994a-460a-8b2e-780a1482d37a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 3%

---

# 反復可能なテクスチャ{#repeatable-textures}

繰り返し可能なテクスチャには、内装材および外装材（布地、アパレルおよび室内装飾材の両方）、壁から壁までの床材、壁紙、カウンタートップ材、木目調、屋根およびサイディング材などの一般的なテクスチャなどがあります。

繰り返し可能なテクスチャは、フラット、フローライン、スケッチ、平面、壁、キャビネットの各オブジェクトに適用できます。 テクスチャを設定できないオブジェクトに適用すると、オブジェクトは `color=` でペイントされます（`color=` が指定されていない場合は `bgc=` でペイントされます）。

マテリアルにイメージを指定する `src=` 属性が含まれ、マテリアルがデカルまたは壁の境界以外の MSS に存在する場合、マテリアルはテクスチャと見なされます。

レンダリング時に、テクスチャ マテリアルの `anchor=` 点とオブジェクトのテクスチャ原点を一致させることにより、テクスチャがオブジェクトに位置合わせされます（ビネットで作成）。

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
   <td colname="col2"> <p>繰り返し可能なテクスチャ イメージ；必須 </p> </td> 
   <td colname="col3"> <p>なし </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャの解像度 </p> </td> 
   <td colname="col3"> <span class="codeph"> 属性：:Resolution </span> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26" type="reference" format="dita" scope="local"> <span class="codeph"> anchor= </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャの位置合わせポイント </p> </td> 
   <td colname="col3"> <p>左上隅 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span> </a> </p> </td> 
   <td colname="col2"> <p>繰り返しモード </p> </td> 
   <td colname="col3"> <p>0 （直線繰り返し） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>シャープ </p> </td> 
   <td colname="col3"> <p>0 （シャープなし）。 </p> </td> 
  </tr> 
 </tbody> 
</table>

これらの基本的なアトリビュートに加えて、繰り返し可能なテクスチャは、高度なアプリケーション用に次の特別な目的のアトリビュートをサポートしています。

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-grout.md#reference-73651cbbbc344adba2626ef950d3672a" type="reference" format="dita" scope="local"> <span class="codeph"> grout= </span> </a> </p> </td> 
   <td colname="col2"> <p>グラウトの色と厚さ。セラミック/石材タイル マテリアルに便利です。 </p> </td> 
   <td colname="col3"> <p>グラウトは既に画像に存在します </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-align.md#reference-4d63baa522ce42f9b15167ba34c5c6a7" type="reference" format="dita" scope="local"> <span class="codeph"> align= </span> </a> </p> </td> 
   <td colname="col2"> <p>位置合わせモード（オブジェクト間）；表皮アプリケーションに使用 </p> </td> 
   <td colname="col3"> <p>中央に一致した </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-rotate.md#reference-3745d74a913e4065b7ac009fb4fd9e3c" type="reference" format="dita" scope="local"> <span class="codeph"> 回転= </span> </a> </p> </td> 
   <td colname="col2"> <p>テクスチャの回転角度。壁オブジェクトではサポートされません。 </p> </td> 
   <td colname="col3"> <p>0 （回転なし） </p> </td> 
  </tr> 
 </tbody> 
</table>
