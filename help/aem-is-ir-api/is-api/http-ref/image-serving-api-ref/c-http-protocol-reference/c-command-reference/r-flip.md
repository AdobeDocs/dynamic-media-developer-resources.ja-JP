---
title: 反転
description: レイヤーを反転。 crop=を適用した後、rotate=および extend=を適用する前に、レイヤーを水平、垂直、またはその両方に反転します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 2%

---

# 反転{#flip}

レイヤーを反転。 crop=を適用した後、rotate=および extend=を適用する前に、レイヤーを水平、垂直、またはその両方に反転します。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを水平方向（左右）に反転します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを垂直方向（上から下）に反転します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>水平方向と垂直方向の両方を反転します。 </p> </td> 
 </tr> 
</table>

テキストレイヤーにも適用できます。

`extend=` などの一部のコマンドは、`layer=comp` を選択すると、複合レイヤーではなくレイヤー 0 に暗黙的に適用されます。 このようなシナリオでは、画層 0 に自動的に割り当てられたすべてのコマンドが、画層 `layer=comp` に適用されるコマンドの前に適用されます。 したがって、`layer=comp` の場合は、`extend=` の前に `flip=` が適用されます。

>[!NOTE]
>
>反転したレイヤーは、レイヤーアンカーに基づいて配置されます。 アンカーがレイヤーの中央にない場合、`flip=` 値が異なると、レイヤーの位置が異なります。

## プロパティ {#section-294da2af7be746b5adfc35e29ee68217}

[ 画層 ] コマンド： 現在のレイヤーまたは合成イメージ（`layer=comp` の場合）に適用されます。 エフェクトレイヤーで無視されます。

## 初期設定 {#section-502044f81a89492198d5f12a738459ea}

なし

## 関連項目 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
