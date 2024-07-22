---
title: op_blur
description: ブラー画像。 画像データにぼかしフィルターを適用します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cd68c109-ee99-4ef7-aac0-7d2e6d408cc0
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '94'
ht-degree: 2%

---

# op_blur{#op-blur}

ブラー画像。 画像データにぼかしフィルターを適用します。

`op_blur= *` 半径 `*`

<table id="simpletable_1DD41D819BE74130A77ECFC28486F70A"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> 半径 </span> </p> </td> 
  <td class="stentry"> <p>ブラーのフィルタ半径（ピクセル単位）（実数 0..100）。 </p></td> 
 </tr> 
</table>

合成画像に対する相対的なピクセル数を *`radius`* します。 レイヤー効果をぼかすために使用されます。

## プロパティ {#section-92573fe2c07746a7bab93a81fc3d208d}

[ 画層 ] コマンド： 現在のレイヤーまたは合成イメージ（`layer=comp` の場合）に適用されます。

## 初期設定 {#section-a976cb86620d489085a8fc9bae2626c0}

ブラー効果を適用しない場合は、`op_blur=0` を使用します。

## 例 {#section-1ebacde68388492eb108ae0fcd7424db}

画像の背景をぼかします。 個別のマスク画像が `catalog::MaskPath` によって参照されます。 `layer=0` を明示的に指定する必要があります。指定しない `op_blur`、合成画像全体に適用されます。

`http://server/myRootId/myImageId?wid=500&layer=0&maskUse=invert&op_blur=20&layer=1&src=myRootId/myImageId`
