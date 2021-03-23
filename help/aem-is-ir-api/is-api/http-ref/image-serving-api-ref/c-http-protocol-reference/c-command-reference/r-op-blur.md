---
description: ぼかし画像。 画像データにぼかしフィルタを適用します。
seo-description: ぼかし画像。 画像データにぼかしフィルタを適用します。
seo-title: op_blur
solution: Experience Manager
title: op_blur
uuid: 8405bbb5-fe09-412e-9b52-0af2c01f48b9
feature: Dynamic Mediaクラシック，SDK/API
role: 開発者、業務従事者
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 2%

---


# op_blur{#op-blur}

ぼかし画像。 画像データにぼかしフィルタを適用します。

`op_blur= *`radius`*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> radius</span> </p> </td> 
  <td class="stentry"> <p>ぼかしフィルターの半径（ピクセル単位、実数0 ～ 100） </p></td> 
 </tr> 
</table>

*`radius`* は、合成画像を基準とするピクセル単位です。レイヤー効果のぼかしにも使用されます。

## プロパティ {#section-92573fe2c07746a7bab93a81fc3d208d}

レイヤーコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。

## 初期設定 {#section-a976cb86620d489085a8fc9bae2626c0}

`op_blur=0`（ぼかし効果なし）。

## 例 {#section-1ebacde68388492eb108ae0fcd7424db}

画像の背景をぼかします。 `catalog::MaskPath`は別のマスク画像を参照します。 `layer=0`は明示的に指定する必要があります。明示的に指定しないと、`op_blur`は合成画像全体に適用されます。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
