---
description: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eb2196cb-b771-4828-8390-cd9e3fe6c57e
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---

# PageView.iconEffect{#pageview-iconeffect}

[!DNL `[PageView.|<containerId>_pageView.]iconeffect=0|1[, *`count`*][, *`fade`*][, *`autoHide`*]`]

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態にあり </span> 画像とのやり取りに使用可能なアクションを示唆する場合に、<span class="codeph"> iconeffect を画像の上部に表示できるようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> 数 </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> iconeffect の表示回数と再表示回数 </span> 最大値を指定します。 値 <span class="codeph">-1</span> は、アイコンが常に無限に再び表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> フェード </span></span> </p> </td> 
   <td colname="col2"> <p>アニメーションの表示または非表示の時間を秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> iconeffect が自動的に非表示になるまでに完全に表示され続ける秒数を設定し </span> す。 つまり、フェードイン アニメーションが完了した後、フェードアウト アニメーションが開始するまでの時間です。 0</span><span class="codeph"> 設定すると、自動非表示動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-b6e5e52698d4492f9d6350e7e312bb1b}

オプション。

## 初期設定 {#section-7d0fc8fa09b34c288ed32ef7faa84604}

[!DNL `1,1,0.3,3`]

## 例 {#section-95db1bfcccf241089654363203b19977}

[!DNL `iconeffect=0`]
