---
description: PageView.iconEffect
solution: Experience Manager
title: PageView.iconEffect
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: eb2196cb-b771-4828-8390-cd9e3fe6c57e
TQID: 'https://experienceleague.adobe.com/vLgMRd56WQf2hBXMvsMN8HEt-hieuMW1D-DgHU5OFWY'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 120
ht-degree: 4%

---

# PageView.iconEffect{#pageview-iconeffect}

[!DNL `[PageView.|<containerId>_pageView.]iconeffect=0|1[, *`count`*][, *` フェード `*][, *`autoHide`*]`]

<table id="table_DD66FFC263A34220876DD204BFE62D49"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> 画像がリセット状態で、画像を操作するアクションが表示されることを示す場合に、画像の上部に<span class="codeph"> iconeffect</span>を表示できるようにします。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> カウント </span></span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> アイコンエフェクト </span>の最大表示回数を指定します。 値<span class="codeph"> -1</span>は、アイコンが常に無期限に再表示されることを示します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> フェード </span></span> </p> </td> 
   <td colname="col2"> <p>表示または非表示のアニメーションのデュレーションを秒単位で指定します。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> autoHide</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> アイコンエフェクト </span>が自動的に非表示になるまでの表示時間を秒単位で設定します。 つまり、フェードインアニメーションが完了してからフェードアウトアニメーションが開始されるまでの時間です。 <span class="codeph"> 0</span>を設定すると、自動非表示の動作が無効になります。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-b6e5e52698d4492f9d6350e7e312bb1b}

オプション。

## 初期設定 {#section-7d0fc8fa09b34c288ed32ef7faa84604}

[!DNL `1,1,0.3,3`]

## 例 {#section-95db1bfcccf241089654363203b19977}

[!DNL `iconeffect=0`]
