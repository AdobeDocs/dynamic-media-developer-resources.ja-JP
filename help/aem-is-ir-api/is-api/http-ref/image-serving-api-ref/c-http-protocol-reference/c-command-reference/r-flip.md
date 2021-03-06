---
description: レイヤを反転 切り抜き=を適用した後、回転=と extend=を適用した後、レイヤーを水平、垂直または両方に反転します。
solution: Experience Manager
title: 反転
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 451d8b4d-0f22-41f3-ac86-435797c23ea3
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---

# 反転{#flip}

レイヤを反転 切り抜き=を適用した後、回転=と extend=を適用した後、レイヤーを水平、垂直または両方に反転します。

`flip=lr|ud|lrud`

<table id="simpletable_072CA0E24B7146D48AEFD70E51E849C2"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> lr </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを水平方向に反転（左右） </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ud </span> </p> </td> 
  <td class="stentry"> <p>レイヤーを垂直方向に反転（上下）します。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> ラウド </span> </p> </td> 
  <td class="stentry"> <p>水平方向と垂直方向の両方を反転します。 </p> </td> 
 </tr> 
</table>

テキストレイヤーにも適用できます。

一部のコマンド ( `extend=`では、 `layer=comp` が選択されている。 この場合、画層 0 に自動的に割り当てられたすべてのコマンドは、適用先のコマンドの前に適用されます。 `layer=comp`. このようにして、 `layer=comp`, `extend=` 次の値より前に適用： `flip=`.

>[!NOTE]
>
>反転レイヤーは、レイヤーアンカーに基づいて配置されます。flip=値が異なると、アンカーがレイヤーの中心にない場合に、レイヤーの位置が異なります。

## プロパティ {#section-294da2af7be746b5adfc35e29ee68217}

[ 画層 ] コマンド 現在の画層または合成画像に適用します ( `layer=comp`. 効果画層で無視されます。

## 初期設定 {#section-502044f81a89492198d5f12a738459ea}

なし

## 関連項目 {#section-47f6484deccd420983df15ec163b4a83}

[rotate=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-rotate.md#reference-12abb086635546ec9ec2e1a793dc1096) , [anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c)
