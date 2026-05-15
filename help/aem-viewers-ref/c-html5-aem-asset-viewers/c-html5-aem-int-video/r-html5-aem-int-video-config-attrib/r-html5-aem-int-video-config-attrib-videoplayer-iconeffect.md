---
title: VideoPlayer.iconeffect
description: インタラクティブビデオビューアの設定属性。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 690dc488-2db0-4166-a308-f1f3438c480a
TQID: 'https://experienceleague.adobe.com/s2UgvZ7USvFjvZ8NBUKa1MHrRe9HOh-ZE-g7jpNyeeg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 3%

---

# VideoPlayer.iconeffect{#videoplayer-iconeffect}

インタラクティブビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect=0|1[, *`count`*][, *` フェード `*][, *`autoHide`*]`

<table id="table_441553CD34C94A58A9D7CBF772DEDDB6"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> ビデオが一時停止している場合に、IconEffectをビデオの上に表示できるようにします。 一部のデバイスでは、ネイティブコントロールが使用されています。 このような場合、<span class="codeph"> iconeffect</span>修飾子は無視されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> カウント </span></span> </p> </td> 
   <td colname="col2"> <p> IconEffectが表示され、再表示される最大回数を指定します。 値<span class="codeph"> -1</span>は、アイコンが無期限に再表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> フェード </span></span> </p> </td> 
   <td colname="col2"> <p> アニメーションを表示または非表示にする時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffectが自動的に非表示になる前に完全に表示される秒数を設定します。 つまり、フェードインアニメーションが完了してからフェードアウトアニメーションが開始されるまでの時間です。 自動非表示の動作を無効にするには、<span class="codeph"> 0</span>に設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-1e637b22e8a44d759d588e47576891e6}

オプション。

## 初期設定 {#section-71fb773f814649b2885aefee68073641}

`1,-1,0.3,0`

## 例 {#section-bce98c31f08a4a0ab262fab7f95ba020}

`iconeffect=0`
