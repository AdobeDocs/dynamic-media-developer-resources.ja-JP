---
title: op_hue
description: 画像の色相を調整します。 レイヤーまたは合成画像の各表示ピクセルの色相を、指定した量だけシフトします。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b436bd31-12a9-42ed-9ad3-5ff91e3ccce9
TQID: 'https://experienceleague.adobe.com/6VSkHDcXsf531qB6okDvLt-xIyFoiw-fG3Z11a-Ne5g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 1%

---

# op_hue{#op-hue}

画像の色相を調整します。 レイヤーまたは合成画像の各表示ピクセルの色相を、指定した量だけシフトします。

`op_hue= *`adj`*`

<table id="simpletable_7DC7ABA384664BDDAA65B8DEEF7859A8"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>色相の調整（度：-180...+180 int） </p></td> 
 </tr> 
</table>

360度の色相範囲に基づいています。

## プロパティ {#section-55779644700b4c808a624cdf5a04447e}

Layer コマンド。 現在のレイヤーまたは`layer=comp`の場合はコンポジット画像に適用されます。 エフェクトレイヤーでは無視されます。 CMYK画像またはレイヤーは、操作が適用される前にRGBに変換されます。

## 初期設定 {#section-7314580251f5456fa1f381ec9e99e0bb}

色相が変更されない`op_hue=0`。
