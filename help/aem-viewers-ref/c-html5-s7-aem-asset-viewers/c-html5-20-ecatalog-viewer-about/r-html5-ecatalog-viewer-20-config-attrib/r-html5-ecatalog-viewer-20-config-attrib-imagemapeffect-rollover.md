---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
topic: Dynamic media
uuid: 92bd8ced-1c41-4147-96fa-5f77bdd6a316
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---


# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>情報パネルを表示するタイミングを指定します。 </p> <p><span class="codeph"> 1</span>に設定した場合、マウスが画像マップ領域に入ると情報パネルが表示されます（画像マップに空でない<span class="codeph"> rollover_key</span>属性が含まれている場合）。 </p> <p><span class="codeph"> 0</span>に設定した場合、画像マップをクリックすると情報パネルがトリガされます（画像マップに空でない<span class="codeph"> rollover_key</span>があり、空の<span class="codeph"> href</span>属性がある場合）。 </p> <p> タッチ対応デスクトップシステムを含むタッチデバイスでは無視され、自動的に<span class="codeph"> 0</span>に設定されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ccfedc2da28f412a86d03f390db92b4b}

（オプション）

## 初期設定 {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## 例 {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
