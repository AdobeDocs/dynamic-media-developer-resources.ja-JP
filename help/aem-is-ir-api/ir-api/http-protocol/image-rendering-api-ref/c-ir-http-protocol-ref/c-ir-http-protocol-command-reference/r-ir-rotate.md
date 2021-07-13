---
description: 材料の回転角度。 マテリアルの回転角度を定義します。
solution: Experience Manager
title: 循環
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 6%

---

# 循環{#rotate}

材料の回転角度。 マテリアルの回転角度を定義します。

` rotate= *`角度`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角度 </span> </p> </td> 
  <td class="stentry"> <p>回転角度（度単位、実数） </p> </td> 
 </tr> 
</table>

繰り返し可能なテクスチャマテリアル（壁紙を除く）を、[フラットオブジェクト]または[平面オブジェクト]に適用した場合に、45度の倍数で回転します。

繰り返し可能なテクスチャマテリアルを、フローラインオブジェクトとスケッチオブジェクトに適用した場合に、任意の角度で回転します。

任意の角度でデカールマテリアルを回転します。

正の角度は時計回りに回転します。 アンカーポイント(`anchor=`)を中心にテクスチャまたはデカールが回転します。アンカーポイントは、ターゲットオブジェクトの原点に位置合わせされたままになります。

## プロパティ {#section-ad4d07897ca24f63af1a4062f8618e36}

マテリアル属性。 べた塗り、壁紙、キャビネット、窓の処理材では無視されます。 *`angle`* 繰り返し可能なテクスチャの場合は、フローラインやスケッチオブジェクトに適用しない限り、45の倍数にする必要があります。

## 初期設定 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0`（回転なし）。

## 関連項目 {#section-f73c00e9368b478dac1fd15bb4367a12}

[アンカー=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
