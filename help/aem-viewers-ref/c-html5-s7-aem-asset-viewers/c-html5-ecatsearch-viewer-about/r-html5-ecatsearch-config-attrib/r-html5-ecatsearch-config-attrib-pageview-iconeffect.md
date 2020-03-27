---
description: 'null'
seo-description: 'null'
seo-title: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
topic: Dynamic media
uuid: c8d63ad9-6867-4b90-a113-6a75e394f706
translation-type: tm+mt
source-git-commit: 2bd5b17e473ec53844b4bbcb4f13580b2d6bfaf4

---


# PageView.iconEffect{#pageview-iconeffect}

[!DNL `[PageView.|<containerId>_pageView.]iconeffect=0|1[, *`countfadeautoHide`*][, *``*][, *``*]`]

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> 画像がリセ <span class="codeph"> ット状態で</span> 、画像の操作に使用できるアクションがある場合に、iconeffectを画像の上部に表示できるようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> カウント</span></span> </p> </td> 
   <td colname="col2"> <p> iconeffectの表示と再表示の最大回 <span class="codeph"> 数を指定</span> します。 値が —1の場合、ア <span class="codeph"> イコンは</span> 常に無限に再表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fade</span></span> </p> </td> 
   <td colname="col2"> <p>表示/非表示のアニメーションの時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p>iconeffectが完全に表示された状態で自動非表 <span class="codeph"> 示にな</span> る秒数を設定します。 つまり、フェードインアニメーションが完了してからフェードアウトアニメーションが開始するまでの時間です。 0に設定すると、自 <span class="codeph"> 動非表</span> 示の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-b6e5e52698d4492f9d6350e7e312bb1b}

（オプション）

## 初期設定 {#section-7d0fc8fa09b34c288ed32ef7faa84604}

[!DNL `1,1,0.3,3`]

## 例 {#section-95db1bfcccf241089654363203b19977}

[!DNL `iconeffect=0`]
