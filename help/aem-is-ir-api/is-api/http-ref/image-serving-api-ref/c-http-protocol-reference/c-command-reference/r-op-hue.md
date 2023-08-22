---
title: op_hue
description: 色相を調整します。 レイヤーまたは合成画像の各表示ピクセルの色相を指定した量ずつシフトします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 1%

---

# op_hue{#op-hue}

色相を調整します。 レイヤーまたは合成画像の各表示ピクセルの色相を指定した量ずつシフトします。

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>色相の調整（度単位 —180...+180 int）。 </p></td> 
 </tr> 
</table>

360 度の色相範囲に基づいています。

## プロパティ {#section-55779644700b4c808a624cdf5a04447e}

[ 画層 ] コマンド 現在の画層または合成画像に適用されます ( `layer=comp`. 効果画層で無視されます。 CMYK 画像またはレイヤーは、操作が適用される前にRGBに変換されます。

## 初期設定 {#section-7314580251f5456fa1f381ec9e99e0bb}

`op_hue=0`（色相を変更しない場合）。
