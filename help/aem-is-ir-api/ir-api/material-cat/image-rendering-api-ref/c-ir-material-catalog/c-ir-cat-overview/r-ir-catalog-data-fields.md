---
title: カタログデータフィールド
description: 次のカタログデータフィールドを使用できます。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bda5fe2d-6205-4737-a9c7-dc934a2d7b06
TQID: 'https://experienceleague.adobe.com/pt6jgwDVUt9beq79ASydG6MRlu42g-guxGHsVj7b-p0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 49c3ac586f6fb17608838f8dcf2c637822314fc7
workflow-type: tm+mt
source-wordcount: 195
ht-degree: 2%

---

# カタログデータフィールド{#catalog-data-fields}

次のカタログデータフィールドを使用できます。

<table id="simpletable_C2D795844F624470871959842AF50BF3"> 
 <thead class="sthead"> 
  <td class="stentry"> <p>カタログ管理 </p></td> 
  <td class="stentry"> <p>説明 </p></td> 
 </thead> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-id.md#reference-cba2a53a952e403fb57a4e8569f9cf85" type="reference" format="dita" scope="local"> Id</a> </p></td> 
  <td class="stentry"> <p>マテリアル識別子（インデックスキー）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319" type="reference" format="dita" scope="local"> TimeStamp</a> </p></td> 
  <td class="stentry"> <p>材料修正タイムスタンプ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-expiration-dataref.md#reference-5e93943abff54c93bf85aae3b911a3ce" type="reference" format="dita" scope="local">有効期限</a> </p></td> 
  <td class="stentry"> <p>クライアントキャッシュの有効期限（有効期間）。 </p></td> 
 </tr> 
</table>

<table id="simpletable_58980295E92848B7BE471855D629F756"> 
 <thead class="sthead"> 
  <td class="stentry"> <p>マテリアル属性 </p></td> 
  <td class="stentry"> <p>説明 </p></td> 
 </thead> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-path.md#reference-59ebb624250a4965ad1737578a2ab590" type="reference" format="dita" scope="local"> パス </a> </p></td> 
  <td class="stentry"> <p>画像データファイルのパスまたはURL。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-auxpath.md#reference-943ad5ee3c3b4b06bbcbb005db0dc969" type="reference" format="dita" scope="local"> AuxPath </a> </p></td> 
  <td class="stentry"> <p>セカンダリデータファイルのパスまたはURL。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-resolution-dataref.md#reference-6a2d64c2d72b438fade58a3391569da7" type="reference" format="dita" scope="local">解決</a> </p></td> 
  <td class="stentry"> <p>画像解像度： </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-anchor.md#reference-d9b1d49db1fc440686f64b84453297ab" type="reference" format="dita" scope="local"> アンカー</a> </p></td> 
  <td class="stentry"> <p>テクスチャ/デカールのアンカーポイント（ホットスポット）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-color.md#reference-7639487fe0ac48beb9e8afa4dc845552" type="reference" format="dita" scope="local"> カラー</a> </p></td> 
  <td class="stentry"> <p>マテリアルカラー： </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-basecolor.md#reference-5f02371b1d8e444ab12d2614d9792de8" type="reference" format="dita" scope="local"> BaseColor </a> </p></td> 
  <td class="stentry"> <p>着色可能なマテリアルの減法線カラー。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-illum.md#reference-faeb85b387544d04b8aa4ccc3ab12e0f" type="reference" format="dita" scope="local"> Illum </a> </p></td> 
  <td class="stentry"> <p>イルミネーションマップセレクター： </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-gloss.md#reference-5277f62a67e2408ab94699aa712f1eeb" type="reference" format="dita" scope="local">光沢</a> </p></td> 
  <td class="stentry"> <p>表面の光沢度： </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-roughness.md#reference-79f748ac642745e3b81795a99f61fa99" type="reference" format="dita" scope="local">粗さ</a> </p></td> 
  <td class="stentry"> <p>サーフェスの粗さ： </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-type.md#reference-9bea147dda9f4e74bc0ec79dcc0d9161" type="reference" format="dita" scope="local"> タイプ </a> </p></td> 
  <td class="stentry"> <p>サーフェスのマテリアルタイプ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-sharp-dataref.md#reference-f79a14bd52474dfd8495115d398a30d0" type="reference" format="dita" scope="local"> シャープ </a> </p></td> 
  <td class="stentry"> <p>テクスチャ/デカールのシャープニング： </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-repeat.md#reference-20e149211e1f4e8285db5ecb83c1902e" type="reference" format="dita" scope="local">繰り返し</a> </p></td> 
  <td class="stentry"> <p>繰り返し可能なテクスチャに対して繰り返しモードを使用します。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-alignment.md#reference-e52152e8dc244d0aa13b40c615d0f399" type="reference" format="dita" scope="local">の整列</a> </p></td> 
  <td class="stentry"> <p>オブジェクト間のテクスチャ整列。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-cat-size.md#reference-a698b0d2652f4ea8a2b006fbf59cf4f1" type="reference" format="dita" scope="local"> サイズ </a> </p></td> 
  <td class="stentry"> <p>デカール/オーバーレイのレイヤーサイズ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-rendersettings-dataref.md#reference-9ce753ae4096455eadcc12ac064de711" type="reference" format="dita" scope="local"> RenderSettings </a> </p></td> 
  <td class="stentry"> <p>高度なレンダリング設定。 </p></td> 
 </tr> 
</table>

<table id="simpletable_BD278D96C3324004ABBBACEDF85F8D50"> 
 <thead class="sthead"> 
  <td class="stentry"> 周辺光量補正</td> 
  <td class="stentry"> <p>説明 </p></td> 
 </thead> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-id-vignette.md#reference-2a7ba758924b4757b3234942304db7fd" type="reference" format="dita" scope="local"> Id</a> </p></td> 
  <td class="stentry"> <p>ビネット識別子（インデックスキー）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1" type="reference" format="dita" scope="local"> TimeStamp</a> </p> </td> 
  <td class="stentry"> <p>周辺光量補正タイムスタンプ。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-expiration-vignette.md#reference-df80829da93e4c0ab3f97a1792d9c74c" type="reference" format="dita" scope="local">有効期限</a> </p></td> 
  <td class="stentry"> <p>クライアントキャッシュの有効期限（有効期間）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-path-vignette.md#reference-aa1c007b63a04351b89881933deaf59c" type="reference" format="dita" scope="local"> パス </a> </p></td> 
  <td class="stentry"> <p>周辺光量補正ファイルのパス </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-modifier.md#reference-cafa1623d65644be8cf3bda6a75ccbc4" type="reference" format="dita" scope="local">修飾子</a> </p></td> 
  <td class="stentry"> <p>定義済みのリクエスト修飾子： </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-userdata.md#reference-5bb5d49aee9c408992e41a5ad17d6e85" type="reference" format="dita" scope="local"> UserData</a> </p></td> 
  <td class="stentry"> <p>ユーザー定義データ： </p></td> 
 </tr> 
</table>

マクロ定義ファイルでは、次のフィールドが認識されます。

<table id="simpletable_B722319F81FB4DDA9AC16B27448B8F04"> 
 <thead class="sthead"> 
  <td class="stentry"> マクロ定義</td> 
  <td class="stentry"> <p>説明 </p></td> 
 </thead> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-macro-definition-reference/r-ir-name.md#reference-63b663d2052545ffab030a23e7060b1e" type="reference" format="dita" scope="local">名</a> </p></td> 
  <td class="stentry"> <p>マクロ名（インデックスキー）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-macro-definition-reference/r-ir-definition.md#reference-8f5a6e146b3b4e598dca1f370acf3bfb" type="reference" format="dita" scope="local">定義</a> </p></td> 
  <td class="stentry"> <p>マクロの定義。 </p></td> 
 </tr> 
</table>

次のフィールドは、ICC カラープロファイルマップファイルで認識されます。

<table id="simpletable_54ED156EDA394412B5C4C49AA3A32828"> 
 <thead class="sthead"> 
  <td class="stentry"> ICC プロファイルマップ</td> 
  <td class="stentry"> <p>説明 </p></td> 
 </thead> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-name-icc.md#reference-7a293ede360e433782575f8f6a562ac2" type="reference" format="dita" scope="local">名</a> </p></td> 
  <td class="stentry"> <p>カラープロファイル名（インデックスキー）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-icc-profile-map-reference/r-ir-profilepath.md#reference-06f756dd364945ee9b50fd94db46e5be" type="reference" format="dita" scope="local"> ProfilePath</a> </p></td> 
  <td class="stentry"> <p>ICC カラープロファイルファイルファイルパス。 </p></td> 
 </tr> 
</table>

