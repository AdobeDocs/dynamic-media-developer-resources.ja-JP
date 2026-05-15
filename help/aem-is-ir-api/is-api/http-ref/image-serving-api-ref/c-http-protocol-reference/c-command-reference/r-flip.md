---
title: 反転
description: レイヤーを反転 crop=を適用した後、rotate=とextend=の前に、レイヤーを水平、垂直、またはその両方に反転します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
TQID: 'https://experienceleague.adobe.com/7RG0rzG40Mp5eQe663S5Ayyf99SIfSLPHgqbSL2Unn4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 157
ht-degree: 2%

---

# 反転{#flip}

レイヤーを反転 crop=を適用した後、rotate=とextend=の前に、レイヤーを水平、垂直、またはその両方に反転します。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを水平方向に反転します（左から右）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを垂直方向に反転します（上下）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lrud </span> </p> </td> 
  <td class="stentry"> <p>水平方向と垂直方向の両方を反転します。 </p> </td> 
 </tr> 
</table>

テキストレイヤーにも適用できます。

`extend=`を含む一部のコマンドは、`layer=comp`を選択すると、合成レイヤーではなくレイヤー0に暗黙的に適用されます。 このようなシナリオでは、レイヤー0に自動的に割り当てられたすべてのコマンドが、適用されるコマンドの前に適用されます。`layer=comp`. したがって、`layer=comp`の場合、`extend=`は`flip=`より前に適用されます。

>[!NOTE]
>
>反転したレイヤーは、レイヤーアンカーに基づいて配置されます。 アンカーがレイヤーの中心にない場合、`flip=`の値が異なると、レイヤーの位置が異なります。

## プロパティ {#section-294da2af7be746b5adfc35e29ee68217}

Layer コマンド。 現在のレイヤーまたは`layer=comp`の場合はコンポジット画像に適用されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-502044f81a89492198d5f12a738459ea}

なし

## 関連項目 {#section-47f6484deccd420983df15ec163b4a83}

[回転=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096)、[ アンカー=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
