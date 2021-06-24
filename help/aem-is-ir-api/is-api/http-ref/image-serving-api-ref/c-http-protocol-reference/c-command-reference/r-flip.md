---
description: レイヤを反転 切り抜き=を適用した後、回転=と延長=を適用した後、レイヤーを水平、垂直または両方に反転します。
solution: Experience Manager
title: 反転
feature: Dynamic Media Classic、SDK/API
role: Developer,Business Practitioner
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 3%

---

# 反転{#flip}

レイヤを反転 切り抜き=を適用した後、回転=と延長=を適用した後、レイヤーを水平、垂直または両方に反転します。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr  </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを水平方向に反転（左右） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud  </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを垂直方向に反転（上下） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ラード  </span> </p> </td> 
  <td class="stentry"> <p>水平方向と垂直方向の両方を反転します。 </p> </td> 
 </tr> 
</table>

また、テキストレイヤーにも適用できます。

`extend=`を含む一部のコマンドは、`layer=comp`を選択した場合に、合成画層ではなく画層0に暗黙的に適用されます。 このシナリオでは、画層0に自動的に割り当てられるすべてのコマンドは、`layer=comp`に適用されるコマンドの前に適用されます。 したがって、`layer=comp`の場合、`flip=`の前に`extend=`が適用されます。

>[!NOTE]
>
>反転レイヤーは、レイヤーアンカーに基づいて配置されます。flip=値が異なると、アンカーがレイヤーの中心にない場合に、レイヤーの位置が異なります。

## プロパティ {#section-294da2af7be746b5adfc35e29ee68217}

レイヤコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤでは無視されます。

## 初期設定 {#section-502044f81a89492198d5f12a738459ea}

なし

## 関連項目 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
