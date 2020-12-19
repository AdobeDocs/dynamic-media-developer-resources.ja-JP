---
description: マテリアルの回転角度 マテリアルの回転角度を定義します。
seo-description: マテリアルの回転角度 マテリアルの回転角度を定義します。
seo-title: 循環
solution: Experience Manager
title: 循環
topic: Scene7 Image Serving - Image Rendering API
uuid: 497cd8ea-c6a4-45d2-b5e0-0898ac00913d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 7%

---


# rotate{#rotate}

マテリアルの回転角度 マテリアルの回転角度を定義します。

` rotate= *`角度`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>回転角度（度単位、実数） </p> </td> 
 </tr> 
</table>

フラットオブジェクトまたは平面オブジェクトに適用した場合、繰り返し可能なテクスチャマテリアル（壁紙を除く）を45度の倍数で回転します。

フローラインとスケッチオブジェクトに適用した場合、繰り返し可能なテクスチャマテリアルを任意の角度で回転させます。

任意の角度でデカールマテリアルを回転します。

正の角度は時計回りに回転します。 アンカーポイント( `anchor=`)を中心にテクスチャまたはデカールが回転します。アンカーポイントは、ターゲットオブジェクトの接触チャネルに合わせた状態が維持されます。

## プロパティ {#section-ad4d07897ca24f63af1a4062f8618e36}

マテリアル属性 べた塗り、壁紙、キャビネット、およびウィンドウ処理マテリアルでは無視されます。 *`angle`* は、繰り返し可能なテクスチャの場合は45の倍数にする必要があります。ただし、フローラインやスケッチオブジェクトに適用される場合は除きます。

## 初期設定 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`に設定します。回転は行われません。

## 関連項目 {#section-f73c00e9368b478dac1fd15bb4367a12}

[アンカー=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
