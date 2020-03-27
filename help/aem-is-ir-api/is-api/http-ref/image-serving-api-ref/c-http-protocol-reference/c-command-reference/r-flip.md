---
description: レイヤーを反転 切り抜き=適用後、回転=適用前、延長=適用後に、レイヤーを水平方向、垂直方向または両方向に反転します。
seo-description: レイヤーを反転 切り抜き=適用後、回転=適用前、延長=適用後に、レイヤーを水平方向、垂直方向または両方向に反転します。
seo-title: 反転
solution: Experience Manager
title: 反転
topic: Scene7 Image Serving - Image Rendering API
uuid: d28631f3-2198-4ba3-ab4b-578832db926e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# flip{#flip}

レイヤーを反転 切り抜き=適用後、回転=適用前、延長=適用後に、レイヤーを水平方向、垂直方向または両方向に反転します。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを水平方向に反転（左右） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ド </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを垂直方向に反転（上下） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ラード </span> </p> </td> 
  <td class="stentry"> <p>水平方向と垂直方向に反転します。 </p> </td> 
 </tr> 
</table>

また、テキストレイヤーにも適用できます。

を選択すると、一部のコ `extend=`マンド（を含む）は、合成画層ではなく、画層0に暗黙的に適用 `layer=comp` されます。 このような場合、レイヤ0に自動的に割り当てられたすべてのコマンドは、に適用されるコマンドの前に適用されま `layer=comp`す。 このように、の `layer=comp`場合は、 `extend=` 前に適用されま `flip=`す。

>[!NOTE]
>
>反転されたレイヤーは、レイヤーアンカーに基づいて配置されます。flip=の値を変えると、アンカーがレイヤーの中央に配置されていない場合、レイヤーの位置が異なります。

## プロパティ {#section-294da2af7be746b5adfc35e29ee68217}

レイヤーコマンド 現在のレイヤーまたは合成画像（の場合）に適用されま `layer=comp`す。 エフェクトレイヤーでは無視されます。

## 初期設定 {#section-502044f81a89492198d5f12a738459ea}

なし

## 関連項目 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
