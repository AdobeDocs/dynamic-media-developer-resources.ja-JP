---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: fd3a1fe47da5ba26b53ea9414bfec1e4c11d7392
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 6%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>情報パネルをいつ表示するかを指定します。 </p> <p>に設定した場合 <span class="codeph"> 1</span>を指定した場合、情報パネルは、マウスが画像マップ領域に入ると表示されます（画像マップに空でない場合）。 <span class="codeph"> rollover_key</span> 属性 ) です。 </p> <p>に設定した場合 <span class="codeph"> 0</span> 情報パネルは、画像マップが選択されたとき ( 画像マップに空でない <span class="codeph"> rollover_key</span> および空 <span class="codeph"> href</span> 属性 ) を参照してください。 </p> <p> タッチ操作対応デスクトップシステムを含むタッチデバイスでは無視され、は自動的にに設定されます <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ccfedc2da28f412a86d03f390db92b4b}

（オプション）

## 初期設定 {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## 例 {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
