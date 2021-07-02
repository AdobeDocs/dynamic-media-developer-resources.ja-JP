---
description: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
feature: Dynamic Media Classic，ビューア，SDK/API，混在メディアセット
role: Developer,Business Practitioner
exl-id: 8371cb69-4cd9-457b-bd8c-e4167fc67600
source-git-commit: bfb350e68d9b7e86cec5ee75fe9280b12ce0e54e
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 4%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> ビデオが一時停止されたときに、ビデオの上にIconEffectを表示できるようにします。 一部のデバイスでは、ネイティブのコントロールが使用されます。 この場合、 <span class="codeph"> iconeffect</span>修飾子は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> count</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffectの表示および再表示の最大回数を指定します。 値<span class="codeph"> -1</span>は、アイコンが無期限に再び表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fade</span> </span> </p> </td> 
   <td colname="col2"> <p> 表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> autoHide</span> </span> </p> </td> 
   <td colname="col2"> <p> IconEffectが自動非表示になるまでの表示秒数を設定します。 つまり、フェードインアニメーションが完了してから、フェードアウトアニメーションが開始するまでの時間です。 <span class="codeph"> 0</span>に設定すると、自動非表示の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
