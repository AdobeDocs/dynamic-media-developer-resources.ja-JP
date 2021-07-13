---
description: 色相を調整します。 レイヤーまたは合成画像の各可視ピクセルの色相を指定した量ずつシフトします。
solution: Experience Manager
title: op_hue
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 2%

---

# op_hue{#op-hue}

色相を調整します。 レイヤーまたは合成画像の各可視ピクセルの色相を指定した量ずつシフトします。

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>色相調整（度単位：-180...+180 int）。 </p></td> 
 </tr> 
</table>

360度の色相範囲に基づいています。

## プロパティ {#section-55779644700b4c808a624cdf5a04447e}

レイヤコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤでは無視されます。 CMYK画像またはレイヤーは、操作が適用される前にRGBに変換されます。

## 初期設定 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`（色相を変更しない）。
