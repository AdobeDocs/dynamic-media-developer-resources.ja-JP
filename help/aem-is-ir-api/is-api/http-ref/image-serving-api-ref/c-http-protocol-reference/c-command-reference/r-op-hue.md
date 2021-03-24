---
description: 色相を調整 レイヤーまたは合成画像の各表示ピクセルの色相を、指定した量だけシフトします。
solution: Experience Manager
title: op_hue
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 2%

---


# op_hue{#op-hue}

色相を調整 レイヤーまたは合成画像の各表示ピクセルの色相を、指定した量だけシフトします。

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>色相調整（度単位）(-180 ～ 180 int) </p></td> 
 </tr> 
</table>

360度の色相範囲に基づきます。

## プロパティ {#section-55779644700b4c808a624cdf5a04447e}

レイヤーコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤーでは無視されます。 CMYK画像またはレイヤーは、操作の適用前にRGBに変換されます。

## 初期設定 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`色相を変えない。
