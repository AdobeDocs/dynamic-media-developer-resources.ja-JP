---
description: 色相を調整 レイヤーまたは合成画像の各表示ピクセルの色相を指定した量だけシフトします。
seo-description: 色相を調整 レイヤーまたは合成画像の各表示ピクセルの色相を指定した量だけシフトします。
seo-title: op_hue
solution: Experience Manager
title: op_hue
topic: Scene7 Image Serving - Image Rendering API
uuid: 23da539e-0192-4dc4-a19b-41aa94a82730
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# op_hue{#op-hue}

色相を調整 レイヤーまたは合成画像の各表示ピクセルの色相を指定した量だけシフトします。

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>色相調整（度単位：-180 ～ 180整数） </p></td> 
 </tr> 
</table>

360度の色相範囲に基づきます。

## プロパティ {#section-55779644700b4c808a624cdf5a04447e}

レイヤーコマンド 現在のレイヤーまたは合成画像（の場合）に適用されま `layer=comp`す。 エフェクトレイヤーでは無視されます。 CMYK画像またはレイヤーは、操作の適用前にRGBに変換されます。

## 初期設定 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`を指定します。色相は変わりません。
