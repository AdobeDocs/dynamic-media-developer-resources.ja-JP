---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 3%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>情報パネルを表示するタイミングを指定します。 </p> <p><span class="codeph">1</span> に設定すると、マウスが画像マップ領域に入ったときに情報パネルが表示されます（画像マップに空でない <span class="codeph"> rollover_key</span> 属性が含まれる場合）。 </p> <p>0<span class="codeph"> 設定すると </span> 画像マップが選択されたときに情報パネルがトリガーされます（画像マップに空でない <span class="codeph"> rollover_key</span> と空の <span class="codeph"> href</span> 属性がある場合）。 </p> <p> タッチ操作対応デスクトップシステムを含むタッチデバイスでは無視され、自動的に <span class="codeph"> 0</span> に設定されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ccfedc2da28f412a86d03f390db92b4b}

オプション。

## 初期設定 {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## 例 {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
