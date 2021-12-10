---
title: PageView.frametransition
description: PageView.frametransition
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 026c2fc5-0460-481c-aca9-ddd25371779c
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# PageView.frametransition{#pageview-frametransition}

` [PageView.|<containerId>_pageView.]frametransition=slide|turn|auto[, *`期間`*]`

<table id="table_625D0EEDA21B46FEA3F5CF7DDF769B50"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> slide|turn|auto</span> </p> </td> 
   <td colname="col2"> <p> フレームの変更時に適用される効果の種類を指定します。 </p> <p> 
     <ul id="ul_4224B7C2722A4185A8BD48703D019AA1"> 
      <li id="li_8482037F8E1C4F11A84DF51790A073FE"> <p><span class="codeph"> スライド</span> は、前のフレームがビューからスライドアウトし、新しいフレームがスライドインして表示するトランジションをアクティブにします。 </p> </li> 
      <li id="li_CE9A99564DF348D0A76AB2A5945155A5"> <p><span class="codeph"> ターン</span> ユーザーが四隅の 1 つをドラッグして、インタラクティブなページ反転を実行できる場合に、ページ反転効果を有効にします。 </p> <p>条件 <span class="codeph"> ターン</span> を使用すると、コンポーネントの外観が <span class="codeph"> pageturnstyle</span> 修飾子と <span class="codeph"> .s7pagedivider</span> CSS クラスは無視されます。 </p> <p>注意：  <p><span class="codeph"> ターン</span> アニメーションは Motorola Xoom ではサポートされていません。 </p> </p> </li> 
      <li id="li_79F85B0429CD4B389399FB3823FE767F"> <p> <span class="codeph"> auto</span> デスクトップシステムではターンフレームトランジションを設定し、タッチデバイスではスライドトランジションを設定します。 </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> 期間</span></span> </p> </td> 
   <td colname="col2"> <p>時間を秒単位で指定します <span class="codeph"> スライド</span> または <span class="codeph"> ターン</span> 遷移効果。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## プロパティ {#section-4d25a3f483834d2b9586fa70270ce6bd}

（オプション）

## 初期設定 {#section-d677f04f1c894966884ce9d77a5ea1c1}

`slide,0.3`

## 例 {#section-b877011e5f6240718e9451be8f622c02}

`frametransition=auto,1`
