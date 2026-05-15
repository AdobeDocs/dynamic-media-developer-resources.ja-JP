---
title: op_blur
description: 画像をぼかす： 画像データにぼかしフィルターを適用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
TQID: 'https://experienceleague.adobe.com/e7GXc5NYZC2Flk0Uf71iw-hi-gPdQk-XldMpPH-DwqM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 2%

---

# op_blur{#op-blur}

画像をぼかす： 画像データにぼかしフィルターを適用します。

`op_blur= *`半径`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname">半径</span> </p> </td> 
  <td class="stentry"> <p>ぼかしフィルターの半径（ピクセル単位）（実数0..100）。 </p></td> 
 </tr> 
</table>

*`radius`*&#x200B;は合成画像に対するピクセル単位です。 レイヤー効果のぼかしを使用します。

## プロパティ {#section-92573fe2c07746a7bab93a81fc3d208d}

Layer コマンド。 現在のレイヤーまたは`layer=comp`の場合はコンポジット画像に適用されます。

## 初期設定 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`、ぼかし効果なし。

## 例 {#section-1ebacde68388492eb108ae0fcd7424db}

画像の背景をぼかす。 別のマスク画像は`catalog::MaskPath`によって参照されています。 `layer=0`を明示的に指定する必要があります。指定しない場合、`op_blur`は合成画像全体に適用されます。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
