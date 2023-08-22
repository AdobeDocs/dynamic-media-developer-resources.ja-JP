---
title: op_contrast
description: コントラストを調整します。 50 %を超える明るさのピクセルの明るさを増やし、50 %未満の明るさのピクセルの明るさを減らすことで、画像のコントラストを調整します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 1%

---

# op_contrast{#op-contrast}

コントラストを調整します。 50 %を超える明るさのピクセルの明るさを増やし、50 %未満の明るさのピクセルの明るさを減らすことで、画像のコントラストを調整します。

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>コントラストの調整 ( パーセント単位 (-100 ～ 100 int))。 </p></td> 
 </tr> 
</table>

## プロパティ {#section-d319ed55057344eab0a3c93f720acdbf}

[ 画層 ] コマンド 現在の画層または合成画像に適用されます ( `layer=comp`. 効果画層で無視されます。

## 初期設定 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`（コントラストの変更なし）。 CMYK 画像またはレイヤーは、操作が適用される前にRGBに変換されます。

## 例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

高画質の画像レイヤーのコントラストとシャープネスを低くして、低画質の背景写真に視覚的に一致させます。

... `&op_blur=3&op_contrast=-12&`

今後のリリースでは、50 %の固定輝度ではなく、画像の中央値の明るさが使用される場合があります。
