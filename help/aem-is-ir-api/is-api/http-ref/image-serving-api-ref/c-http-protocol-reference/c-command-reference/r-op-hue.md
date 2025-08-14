---
title: op_hue
description: イメージの色相を調整します。 レイヤーまたは合成画像の表示可能な各ピクセルの色相を、指定した量だけシフトします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 1%

---

# op_hue{#op-hue}

イメージの色相を調整します。 レイヤーまたは合成画像の表示可能な各ピクセルの色相を、指定した量だけシフトします。

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>色相の調整（度単位）（–180...+180 int）。 </p></td> 
 </tr> 
</table>

360 度の色相範囲に基づきます。

## プロパティ {#section-55779644700b4c808a624cdf5a04447e}

[ 画層 ] コマンド： 現在のレイヤーまたは合成イメージ（`layer=comp` の場合）に適用されます。 エフェクトレイヤーで無視されます。 操作を適用する前に、CMYK 画像またはレイヤーがRGBに変換されます。

## 初期設定 {#section-7314580251f5456fa1f381ec9e99e0bb}

色相の変化がない場合は `op_hue=0` を使用します。
