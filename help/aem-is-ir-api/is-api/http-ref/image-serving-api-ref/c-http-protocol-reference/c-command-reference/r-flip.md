---
title: 反転
description: レイヤを反転 切り抜き=を適用した後、回転=と extend=を適用した後、レイヤーを水平、垂直または両方に反転します。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# 反転{#flip}

レイヤを反転 切り抜き=を適用した後、回転=と extend=を適用した後、レイヤーを水平、垂直または両方に反転します。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを水平方向に反転します（左右）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを垂直方向（上下）に反転します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ラウド </span> </p> </td> 
  <td class="stentry"> <p>水平方向と垂直方向の両方を反転します。 </p> </td> 
 </tr> 
</table>

また、テキストレイヤーにも適用できます。

一部のコマンド ( `extend=`を指定した場合に、合成レイヤーではなくレイヤー 0 に暗黙的に適用されます。 `layer=comp` が選択されている。 この場合、画層 0 に自動的に割り当てられたすべてのコマンドは、適用先のコマンドの前に適用されます。 `layer=comp`. このようにして、 `layer=comp`, `extend=` 次の値より前に適用： `flip=`.

>[!NOTE]
>
>反転レイヤーは、レイヤーアンカーに基づいて配置されます。 異なる `flip=` アンカーがレイヤーの中心にない場合、の値によってレイヤーの位置が異なります。

## プロパティ {#section-294da2af7be746b5adfc35e29ee68217}

[ 画層 ] コマンド 現在の画層または合成画像に適用されます ( `layer=comp`. 効果画層で無視されます。

## 初期設定 {#section-502044f81a89492198d5f12a738459ea}

なし

## 関連項目 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
