---
description: ControlBar.transition
solution: Experience Manager
title: ControlBar.transition
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 2e08a62b-9499-41f8-927b-89bed972b4eb
TQID: 'https://experienceleague.adobe.com/bcpeaqLRZ8ClN2OulOfO9ujXzz44Yb2HTmy-GyPQ8mU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
ht-degree: 2%

---

# ControlBar.transition{#controlbar-transition}

[!DNL ` [ControlBar.|<containerId>_controls.]transition=none|fade[, *`delaytohide`*[, *`duration`*]`]

<table id="table_F71AA834FE494949A2D4B569EA5E721F"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|フェード </span> </p> </td> 
   <td colname="col2"> <p> コントロールバーとそのコンテンツの表示/非表示に使用するエフェクトタイプを指定します。 <span class="codeph"> none </span>を使用してインスタントショーと非表示を切り替えます。<span class="codeph"> フェード </span>は、徐々にフェードインとフェードアウト効果を提供します（Internet Explorer 8ではサポートされていません）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">さんが</span> </span>を非表示にするのを遅らせる </p> </td> 
   <td colname="col2"> <p> コントロールバーが登録した最後のマウス/タッチイベントとタイムコントロールバーが非表示になるまでの時間を秒単位で指定します。 </p> <p> <span class="codeph"> -1 </span>に設定した場合、コンポーネントは自動非表示エフェクトをトリガーせず、常に画面に表示されます。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname">期間</span> </span> </p> </td> 
   <td colname="col2"> <p> フェードインとフェードアウトのアニメーションのデュレーションを秒単位で設定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-f42369774e2740dcb399626a0e4e930e}

オプション。 コントロールバーの自動非表示が無効になっているタッチデバイスでは、このコマンドは無視されます。

## 初期設定 {#section-d016470e92a74f98a18c4ab3489410a5}

[!DNL `fade,2,0.5`]

## 例 {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

[!DNL `transition=none`]
