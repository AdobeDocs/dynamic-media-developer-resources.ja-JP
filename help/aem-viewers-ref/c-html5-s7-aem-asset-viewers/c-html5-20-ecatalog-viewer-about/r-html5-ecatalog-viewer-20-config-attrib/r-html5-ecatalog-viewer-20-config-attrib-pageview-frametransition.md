---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 3%

---

# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`duration`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|turn|auto</span> </p> </td> 
   <td colname="col2"> <p> フレーム変更時に適用する効果のタイプを指定します。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> slide</span> 古いフレームが画面外にスライドし、新しいフレームが画面内にスライドするトランジションをアクティブにします。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p>次に </span> ユーザー <span class="codeph"> スプレッドの 4 つの角をドラッグしてインタラクティブなページ反転を実行できる場合に、ページ反転効果を有効にします。 </p> <p>順番 <span class="codeph"> 使用する場合 </span> コンポーネントの外観は <span class="codeph"> pageturnstyle</span> 修飾子で制御され、<span class="codeph"> .s7pagedivider</span> CSS クラスは無視されます。 </p> <p>注意：  <p><span class="codeph"> た </span>Motorola Xoom ではアニメーションはサポートされていません。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> 自動 <span class="codeph"> は </span> デスクトップシステムのターンフレームトランジションとタッチデバイスのスライドトランジションを設定します。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> duration</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> のスライドの表示時間 </span> または切り替え効果 <span class="codeph"> 秒単位 </span> 指定します。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4d25a3f483834d2b9586fa70270ce6bd}

オプション。

## 初期設定 {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## 例 {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
