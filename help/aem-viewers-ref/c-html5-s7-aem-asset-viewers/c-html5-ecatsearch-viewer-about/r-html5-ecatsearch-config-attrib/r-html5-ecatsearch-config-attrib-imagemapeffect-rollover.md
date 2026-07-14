---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
TQID: 'https://experienceleague.adobe.com/V5KPk6tOhMcCUtL7iraaeBNt4xp81Uo7FTpT-1Z44ks'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 87
ht-degree: 5%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p>情報パネルの表示時間を指定します。 </p> <p><span class="codeph"> 1</span>に設定すると、マウスが画像マップ領域に入ると、情報パネルが表示されます（画像マップに空でない場合は、<span class="codeph"> rollover_key</span>属性）。 </p> <p><span class="codeph"> 0</span>に設定すると、画像マップが選択されたときに情報パネルがトリガーされます（画像マップに空でない<span class="codeph"> rollover_key</span>と空の<span class="codeph"> href</span>属性がある場合）。 </p> <p> タッチ対応デスクトップシステムを含むタッチデバイスでは無視され、自動的に<span class="codeph"> 0</span>に設定されます。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-ccfedc2da28f412a86d03f390db92b4b}

オプション。

## 初期設定 {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## 例 {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
