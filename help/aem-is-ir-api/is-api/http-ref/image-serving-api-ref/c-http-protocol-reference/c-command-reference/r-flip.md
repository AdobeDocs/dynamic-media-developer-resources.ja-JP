---
description: レイヤーを反転 切り抜き=を適用した後、回転=と延長=を適用した後に、レイヤーを水平方向、垂直方向または両方向に反転します。
seo-description: レイヤーを反転 切り抜き=を適用した後、回転=と延長=を適用した後に、レイヤーを水平方向、垂直方向または両方向に反転します。
seo-title: 反転
solution: Experience Manager
title: 反転
topic: Dynamic Media Image Serving - Image Rendering API
uuid: d28631f3-2198-4ba3-ab4b-578832db926e
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---


# flip{#flip}

レイヤーを反転 切り抜き=を適用した後、回転=と延長=を適用した後に、レイヤーを水平方向、垂直方向または両方向に反転します。

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
  <td class="stentry"> <p>水平方向と垂直方向の両方に反転します。 </p> </td> 
 </tr> 
</table>

また、テキストレイヤーにも適用できます。

`extend=`を含む一部のコマンドは、`layer=comp`が選択された場合に、複合レイヤーではなくレイヤー0に暗黙的に適用されます。 このような場合、画層0に自動的に割り当てられるすべてのコマンドは、`layer=comp`に適用されるコマンドの前に適用されます。 したがって、`layer=comp`の場合、`flip=`の前に`extend=`が適用されます。

>[!NOTE]
>
>反転したレイヤーは、レイヤーアンカーに基づいて配置されます。flip=の値を変えると、アンカーがレイヤーの中心にない場合に、レイヤーの位置が異なります。

## プロパティ {#section-294da2af7be746b5adfc35e29ee68217}

レイヤーコマンド `layer=comp`の場合は、現在のレイヤーまたは合成画像に適用されます。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-502044f81a89492198d5f12a738459ea}

なし

## 関連項目 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) ,  [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
