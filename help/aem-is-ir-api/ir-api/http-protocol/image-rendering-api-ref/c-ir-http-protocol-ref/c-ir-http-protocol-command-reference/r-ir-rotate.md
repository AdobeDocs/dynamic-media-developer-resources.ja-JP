---
title: 循環
description: 材料の回転角度。 材料の回転角度を定義します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 355d9691-c04b-44a6-9563-5bef185cfa7e
TQID: 'https://experienceleague.adobe.com/prSGGMuV4SpFfhd8uCVzMRGpr-VBpowxE-UagKtpnqI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 4%

---

# 循環{#rotate}

材料の回転角度。 材料の回転角度を定義します。

` rotate= *`角度`*`

<table id="simpletable_F1A87ECD86E8429788825374A6882CB9"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname">角度</span> </p> </td> 
  <td class="stentry"> <p>回転角度（実数）。 </p> </td> 
 </tr> 
</table>

平らなオブジェクトまたは平面オブジェクトに適用した場合、繰り返し可能なテクスチャのマテリアル（壁紙を除く）を45°の倍数で回転させます。

フローラインおよびスケッチオブジェクトに適用した場合、繰り返し可能なテクスチャのマテリアルを任意の角度で回転します。

デカールのマテリアルを任意の角度で回転させます。

正の角度は時計回りに回転します。 テクスチャまたはデカールはアンカーポイント（`anchor=`）を中心に回転します。アンカーポイントはターゲットオブジェクトの原点に沿ったままです。

## プロパティ {#section-ad4d07897ca24f63af1a4062f8618e36}

マテリアル属性： 単色、壁紙、キャビネット、およびウィンドウ処理材料によって無視されます。*`angle`* 繰り返し可能なテクスチャの場合は、フローラインまたはスケッチオブジェクトに適用しない限り、45の倍数にする必要があります。

## 初期設定 {#section-14c991e71b74449db8ff18a775949b28}

`rotate=0` （回転なし）。

## 関連項目 {#section-f73c00e9368b478dac1fd15bb4367a12}

[anchor=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-anchor.md#reference-d53923d785c9442997dc7f2199524c26)
