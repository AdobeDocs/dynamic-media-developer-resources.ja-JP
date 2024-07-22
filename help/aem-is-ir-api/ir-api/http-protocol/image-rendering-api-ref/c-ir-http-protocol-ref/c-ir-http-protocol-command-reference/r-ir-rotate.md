---
title: 循環
description: 材料の回転角度。 マテリアルの回転角度を定義します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 4%

---

# 循環{#rotate}

材料の回転角度。 マテリアルの回転角度を定義します。

` rotate= *` 角度 `*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> 角 </span> </p> </td> 
  <td class="stentry"> <p>回転角度（度単位、実数） </p> </td> 
 </tr> 
</table>

平面オブジェクトまたは平面オブジェクトに適用した場合、繰り返し可能なテクスチャ マテリアル（壁紙を除く）を 45 度の倍数で回転します。

フローラインおよびスケッチ オブジェクトに適用する際に、繰り返し可能なテクスチャ マテリアルを任意の角度で回転します。

デカル転写マテリアルを任意の角度で回転します。

正の角度は時計回りに回転します。 テクスチャまたはデカールは、アンカーポイント（`anchor=`）を中心に回転します。アンカーポイントは、ターゲット オブジェクトの原点に位置合わせされたままになります。

## プロパティ {#section-ad4d07897ca24f63af1a4062f8618e36}

マテリアル アトリビュート。 単色、壁紙、キャビネット、窓処理マテリアルでは無視されます。 フローラインまたはスケッチ オブジェクトに適用する場合を除き、繰り返し可能なテクスチャには 45 の倍数を *`angle`* します。

## 初期設定 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0` （回転なし）。

## 関連項目 {#section-f73c00e9368b478dac1fd15bb4367a12}

[アンカー=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
