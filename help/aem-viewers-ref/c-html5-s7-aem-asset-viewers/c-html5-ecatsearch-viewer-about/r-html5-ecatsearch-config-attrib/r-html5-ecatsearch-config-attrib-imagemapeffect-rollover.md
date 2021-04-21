---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 5%

---


# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

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

[!DNL `0`]

## 例 {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
