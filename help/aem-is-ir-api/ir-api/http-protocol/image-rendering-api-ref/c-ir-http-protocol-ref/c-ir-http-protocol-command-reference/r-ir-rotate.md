---
description: マテリアルの回転角度。 マテリアルの回転角度を定義します。
seo-description: マテリアルの回転角度。 マテリアルの回転角度を定義します。
seo-title: 循環
solution: Experience Manager
title: 循環
topic: Scene7 Image Serving - Image Rendering API
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# rotate{#rotate}

マテリアルの回転角度。 マテリアルの回転角度を定義します。

` rotate= *`角度`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>回転角度（度単位、実数） </p> </td> 
 </tr> 
</table>

繰り返し可能なテクスチャマテリアル（壁紙を除く）を、フラットオブジェクトまたは平面オブジェクトに適用した場合に、45度の倍数で回転させます。

繰り返し可能なテクスチャマテリアルを、フローラインおよびスケッチオブジェクトに適用した場合に、任意の角度で回転させます。

任意の角度でデカルのマテリアルを回転します。

正の角度は時計回りに回転します。 テクスチャまたはデカールがアンカーポイント( `anchor=`)を中心に回転します。アンカーポイントは、ターゲットオブジェクトの原点に揃えられたままになります。

## プロパティ {#section-ad4d07897ca24f63af1a4062f8618e36}

マテリアル属性。 べた塗り、壁紙、キャビネット、および窓の処理マテリアルでは無視されます。 *`angle`* は、繰り返し可能なテクスチャの場合は、フローラインまたはスケッチオブジェクトに適用しない限り、45の倍数である必要があります。

## 初期設定 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`を指定します。回転は使用しません。

## 関連項目 {#section-f73c00e9368b478dac1fd15bb4367a12}

[アンカー=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
