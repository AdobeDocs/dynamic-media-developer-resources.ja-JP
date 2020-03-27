---
description: ビデオビューアの設定属性。
seo-description: ビデオビューアの設定属性。
seo-title: VideoPlayer.iconeffect
solution: Experience Manager
title: VideoPlayer.iconeffect
topic: Dynamic media
uuid: 1ba6f24a-77bb-41ef-a831-a7ac817abd73
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# VideoPlayer.iconeffect{#videoplayer-iconeffect}

ビデオビューアの設定属性。

` [VideoPlayer.|<containerId>_videoPlayer.]iconeffect= *`0|1`*[, *``*][, *``*][, *`countfadeautoHide`*]`

<table id="table_C616483932C2482CA9794DDD7313FD7C"> 
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

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

（オプション）

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

`1,-1,0.3,0`

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
iconeffect=0
```

