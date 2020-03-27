---
description: 'null'
seo-description: 'null'
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 8e112f3c-8fa6-4c77-94c5-5027275225e7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_38995A95977645AD8716203987DD9909"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 0|1</span> </span> </p> </td> 
   <td colname="col2"> <p> ビデオが一時停止されたときに、IconEffectがビデオの上に表示されるようにします。 一部のデバイスでは、ネイティブのコントロールが使用されます。 この場合、iconeffect修飾子は <span class="codeph"> 無視され</span> ます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 数</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffectの表示と再表示の最大回数を指定します。 値が —1の場合、ア <span class="codeph"> イコンは</span> 無期限に再表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> フェー <span class="varname"> ド</span></span> </p> </td> 
   <td colname="col2"> <p> 表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 自動非 <span class="varname"> 表示</span></span> </p> </td> 
   <td colname="col2"> <p> IconEffectが自動的に非表示になるまでの表示秒数を設定します。 つまり、フェードインアニメーションが完了してから、フェードアウトアニメーションが開始するまでの時間です。 0に設定すると、自 <span class="codeph"> 動非表示</span> の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-65be9301796240e38f31818229da7acc}

（オプション）

## 初期設定 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`1,-1,0.3,0`

## 例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`iconeffect=0`
