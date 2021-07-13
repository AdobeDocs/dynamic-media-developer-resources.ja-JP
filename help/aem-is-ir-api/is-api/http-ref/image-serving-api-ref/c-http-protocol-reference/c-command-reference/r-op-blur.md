---
description: ぼかし画像。 画像データにぼかしフィルターを適用します。
solution: Experience Manager
title: op_blur
feature: Dynamic Media Classic、SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 3%

---

# op_blur{#op-blur}

ぼかし画像。 画像データにぼかしフィルターを適用します。

`op_blur= *`radius`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>ぼかしフィルタの半径（ピクセル単位、実数0 ～ 100）。 </p></td> 
 </tr> 
</table>

*`radius`* は、合成画像を基準とするピクセル単位です。レイヤー効果のぼかしにも使用されます。

## プロパティ {#section-92573fe2c07746a7bab93a81fc3d208d}

レイヤコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。

## 初期設定 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`（ぼかし効果なし）。

## 例 {#section-1ebacde68388492eb108ae0fcd7424db}

画像の背景をぼかします。 `catalog::MaskPath`は別のマスク画像を参照します。 `layer=0`を明示的に指定する必要があります。そうしないと、 `op_blur`が合成画像全体に適用されます。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
