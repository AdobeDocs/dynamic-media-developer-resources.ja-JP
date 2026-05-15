---
title: op_contrast
description: コントラストを調整します。 明るさが50%を超えるピクセルの明るさを上げ、明るさが50%未満のピクセルの明るさを下げて、画像コントラストを調整します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0216f22e-a3b3-4dda-89c2-9c6c2c81cab3
TQID: 'https://experienceleague.adobe.com/Ob098G38TFXX0HzB3JQOCcdD9ZnrYWrMum6XEQSmGRU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 143
ht-degree: 1%

---

# op_contrast{#op-contrast}

コントラストを調整します。 明るさが50%を超えるピクセルの明るさを上げ、明るさが50%未満のピクセルの明るさを下げて、画像コントラストを調整します。

`op_contrast= *`adj`*`

<table id="simpletable_8246802C74424A68A7A2EA5B50A89D42"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> adj</span> </p> </td> 
  <td class="stentry"> <p>コントラスト調整（–100...100 int） </p></td> 
 </tr> 
</table>

## プロパティ {#section-d319ed55057344eab0a3c93f720acdbf}

Layer コマンド。 現在のレイヤーまたは`layer=comp`の場合はコンポジット画像に適用されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-896d1b1f7f084e929355a4684f3e833b}

`op_contrast=0`、コントラストに変化はありません。 CMYK画像またはレイヤーは、操作が適用される前にRGBに変換されます。

## 例 {#section-94bc4348b4bc4f0e9768ea1c45ca8340}

高画質の画像レイヤーのコントラストとシャープを下げて、低画質の背景写真に視覚的に一致させます。

... `&op_blur=3&op_contrast=-12&`

将来のリリースでは、固定の50%の明るさではなく、画像の中央値の明るさを使用する場合があります。
